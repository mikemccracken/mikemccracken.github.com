---
comments: true
date: 2006-05-23 23:30:14
layout: post
slug: xcode-23-hidden-gem-interface-builder-254
title: 'XCode 2.3 Hidden Gem: Interface Builder 2.5.4'
wordpress_id: 46
categories:
- mac
- programming
---

XCode 2.3 is out, so why not spend a nice May evening reading some [Dev Tools release notes][0]?

There are some excited posts about Dedicated Network Builds from [people who work at Apple][1], but not having a cluster of build machines myself, I'm not so worked up. (Unless sourceforge gets on that for their build farm.)

Then I saw this one line buried a little past halfway through:

* Nibtool
 * Added functionality for exporting and importing properties as a plist
Nibtool can extract properties into a plist format that can be edited and then reimported into the nib using the new --export (-e) and --import (-i) flags.

If I read this right, it means the door is open for easy automated access to bindings and maybe a way to make editing bindings easier. I know visual programming has its benefits, but bindings are just so *opaque* - you see one object's binding at a time, and making mass changes to bindings is just impossible - *until now, I hope*.

I'm downloading it now.

[0]:http://developer.apple.com/tools/xcode/update.html
[1]:http://chanson.livejournal.com/145343.html
