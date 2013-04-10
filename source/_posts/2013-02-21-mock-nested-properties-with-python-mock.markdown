---
layout: post
title: "Mock nested properties with python-mock"
date: 2013-02-21 15:05
comments: true
categories: 
---

Python's [mock][mock] library (part of stdlib in 3.3+) is a great tool for writing concise tests.
Its documentation is very good, and rewards multiple reads - but I found one thing that wasn't totally clear, even after looking through a few times.
I wanted to use PropertyMock to mock nested Properties. Specifically, I had patched the python Gnome-introspection wrapper for libsoup at the top level `Soup` objcet, and I also wanted to replace one of its nested constant properties, Soup.MemoryUse.COPY with a sentinel that I controlled, for later comparison. 

The idiom for PropertyMock is to assign a PropertyMock to the type object of the Mock object whose property you want control of.
What I found is that because Mocks auto-create properties, it's possible to do nested mocking in one line, like this:

{% codeblock lang:python %}
import mock
m = mock.Mock()
type(m.a.b.c).d = mock.PropertyMock(return_value = mock.sentinel.my_value)
assert(m.a.b.c.d == mock.sentinel.my_value)
{% endcodeblock %}

So my soup example looks roughly like this (mixing testing and tested code, and repeating literals for brevity):
{% codeblock lang:python %}
json_body = "{}"
with patch(gi.repository.Soup) as mock_soup:
    from gi.repository import Soup
    type(mock_soup.MemoryUse).COPY = mock.PropertyMock(return_value=mock.sentinel.COPY)

    # tested code:
    message = Soup.Message.new("POST", "http://fake.com/api")
    message.set_request('application/json', Soup.MemoryUse.COPY, json_body, len(json_body))

    # checking:
    assert(mock_soup.mock_calls == [mock.call.Message.new("POST", "http://fake.com/api"), 
                                    mock.call.Message.new().set_request('application/json', 
                                                                        sentinel.COPY # <--- this was the point
                                                                        "{}", 2)])
{% endcodeblock %}

It's often possible to think of a shorter, clearer use of the mock library after revisiting a problem, but so far this still seems good. Let me know in the comments if you have a suggestion for improvements.

[mock]:http://www.voidspace.org.uk/python/mock/
