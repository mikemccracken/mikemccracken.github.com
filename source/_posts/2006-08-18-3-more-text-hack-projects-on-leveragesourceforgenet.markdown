---
comments: true
date: 2006-08-18 15:59:20
layout: post
slug: 3-more-text-hack-projects-on-leveragesourceforgenet
title: 3 more text hack projects on leverage.sourceforge.net
wordpress_id: 61
categories:
- mac
- me
- programming
---

13 months ago, I ["launched"][levann] the [leverage project](http://leverage.sourceforge.net) on sourceforge, supposed to be a place to house all the various OS X / Cocoa text manipulation hacks I've done, including my I-Search for NSTextView InputManager hack.

I haven't touched leverage since, but today I added three more projects to the SVN repository with varying appeal and usability. I also added a mailing list, [leverage-discuss](https://lists.sourceforge.net/lists/listinfo/leverage-discuss).

If you're interested in trying these out or working on one of these hacks, and want to ask a question, using that email list would be best, but you can also [email me](mailto:michael_mccracken@mac.com) directly about them.

#### TextShape

Here's my 2004 blog post about it: ["Usability and Editing Code: TextShapeView"](http://michael-mccracken.net/blog/blosxom.pl/computers/mac/programming/meetTSV.html) and here's the old home page for it, with a screenshot: [TextShapeView](http://michael-mccracken.net/?TextShapeView).

The code is unchanged, but it works fine on 10.4.

[http://svn.sourceforge.net/viewvc/leverage/textshape/trunk/](http://svn.sourceforge.net/viewvc/leverage/textshape/trunk/)

#### TextStructure

A long time ago, so long I can't even find it with google, I posted somewhere about a hacked version of [TexShop](http://darkwing.uoregon.edu/~koch/texshop) that had an outline view in a drawer that showed the section structure of your TeX document.

I never got that working well enough to try adding it to TexShop, but I did realize that it's something that could be useful for other kinds of text as well.

A big project, the TextStructure InputManager adds a key binding to NSTextView that pops up a window with an outline view that tries to represent the current text as an outline, using a scheme of regular expressions that mark some lines of text as "tags" with outline levels, depending on the text. It has a few regexps built in for LaTeX, ObjC, TODO & FIXME lines, and email quoting (which doesn't quite make sense).

You can also search the text for a regexp, and it will highlight the sections which contain a match.

I don't have a screenshot just yet, but I'll post about it more later.

[http://svn.sourceforge.net/viewvc/leverage/textstructure/trunk/](http://svn.sourceforge.net/viewvc/leverage/textstructure/trunk/)

#### OEM : Open in Emacs

This is a new one, and a work-in-progress. It adds a key binding to open the text of the current text view in an emacs buffer, using a temporary file and `emacsclient`. It currently has no way to get the text back into the text view from the file when you're done editing it in emacs, and doesn't delete the file. But it's at least partially nifty...

[http://svn.sourceforge.net/viewvc/leverage/oem/trunk/](http://svn.sourceforge.net/viewvc/leverage/oem/trunk/)

#### ISIM: Incremental Search in NSTextView

Not new, but it's in there too:
[http://svn.sourceforge.net/viewvc/leverage/isim/trunk/](http://svn.sourceforge.net/viewvc/leverage/isim/trunk/)


[levann]:http://michael-mccracken.net/blog/blosxom.pl/computers/mac/programming/meetLeverage.html
