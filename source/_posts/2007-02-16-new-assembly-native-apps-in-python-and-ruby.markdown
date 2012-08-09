---
comments: true
date: 2007-02-16 13:26:49
layout: post
slug: new-assembly-native-apps-in-python-and-ruby
title: '"New Assembly?" - native apps in Python and Ruby?'
wordpress_id: 89
---

A couple days ago, Daniel Jalkut wrote a [quick note][dj-cna] wondering if the future is writing native desktop apps in languages like Python or Ruby, dropping down into C/Obj-C only for performance reasons. It's been an interesting thread since then, in comments and other posts.
Notably, today Bill Bumgarner responded with a [long and informative ramble][bb] about how the dynamic language future is already here.

Specifically, he notes that the Python-ObjC bridge has been working for quite some time, and is even in use by a few commercial apps.

As official support for this kind of development grows, I bet we'll  find more apps written with mostly Python (or Ruby) and a few ObjC/C/C++ bundles or frameworks. I really don't think this will be a performance problem - from what I can tell, performance problems in desktop apps are more often algorithm problems or I/O problems - overheads of small constant factors due to using an interpreted language are in the wash.

I've probably written as much Python (not using the bridge) as Objective-C, and my experience is that I feel like I'm solving the problem faster with Python. I particularly like the more compact syntax for common data structures like lists, dictionaries and tuples - I've written and modified a couple of very small Cocoa apps using PyObjC (including Python plugins for VoodooPad), and it feels like I'm getting away with something when I pass inline lists + dictionaries to AppKit...

In case you're wondering about what Py-Cocoa code looks like, there are a lot of great [examples](http://pyobjc.sourceforge.net/examples/index.php) on the PyObjC project site. Looking at it now, it's like I'm reading Cocoa email-pseudocode, and I like that.

[dj-cna]:http://www.red-sweater.com/blog/278/c-is-the-new-assembly
[bb]:http://www.friday.com/bbum/2007/02/16/c-portable-macro-assembler/
