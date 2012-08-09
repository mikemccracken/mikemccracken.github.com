---
comments: true
date: 2009-09-18 12:36:57
layout: post
slug: better-svn-workflow-in-emacs
title: 'Better SVN workflow in Emacs '
wordpress_id: 201
tags:
- emacs
- svn
- vc
- workflow
---

I've found a way to get the 3-column window layout with vc-dir, vc-diff and vc-log I showed in my [previous post about SVN workflow in Emacs](http://michael-mccracken.net/wp/?p=144) by default, without the manual setup I was complaining about. 

(*Update*: It looks like this customization only exists in Emacs 23.)

The key is that vc-mode uses a standard function, `pop-to-buffer`, to create the new window for vc-diff and vc-log. This is the function that keeps creating horizontal splits that make no sense on my widescreen display. However, it ends up calling a function called `split-window-sensibly`, which can be customized (of course!). So, if I set the "Split Height Threshold" to nil, `split-window-sensibly` will never split horizontally, and then the default behavior just magically does what I want. If I start with just a single vc-dir window and invoke vc-diff and vc-log, I get my three columns!

To get to the right customization screen, just do `M-x customize-apropos <ret> ^Split.*Threshold`. That'll get you the two relevant customization items. Enjoy!
