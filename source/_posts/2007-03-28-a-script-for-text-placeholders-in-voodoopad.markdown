---
comments: true
date: 2007-03-28 10:59:47
layout: post
slug: a-script-for-text-placeholders-in-voodoopad
title: A script for text placeholders in VoodooPad
wordpress_id: 96
categories:
- mac
- scripts
- tips
- VoodooPad
---

Last year I wrote about my [new page template for VoodooPad](http://michael-mccracken.net/wp/?p=39). I still use something like it - I like the uniform look and the built-in navigation starters I get in every page.

I got tired of all the clicking around it took to fill in the navigation every time I put in a new page, so I decided to write a script to mimic XCode's "Select Next Placeholder" command. In XCode, if you use code completion, you might get something like this:
`[dict setObject:<# (id) anObject #> forKey:<# (id)key #>]` Then pressing Control-/ cycles the selection through those placeholders so you can replace them with whatever you want quickly.

That's really handy for code, and it's great for VoodooPad templates too. I wrote the script as a Python script plugin for VoodooPad, and it maps Command-/ to select the next placeholder, wrapping the search at the end just like XCode does. Now my new page template in VoodooPad has a few placeholders in it, and I have a lot fewer pages with default template text sitting in there making me look lazy.

Download it [here](http://michael-mccracken.net/2007/Select-Next-Placeholder.py). (Note, it needs the [VoodooPad Python Plugin Enabler](http://flyingmeat.com/fs/flystashweb.cgi/40de692c-e33c-01d9-12a1-c0cbe4c4d9e7) )
