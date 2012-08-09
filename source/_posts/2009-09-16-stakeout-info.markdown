---
comments: true
date: 2009-09-16 21:42:59
layout: post
slug: stakeout-info
title: Stakeout info
wordpress_id: 188
tags:
- kqueue
- stakeout
- testing
---

This post is here to prevent broken links, since I've noticed people coming here from a link to my old Stakeout page.

Stakeout was a program that runs something when files change, by watching for file changes at the system level using kqueue. It was intended to support running automated tests. The 2nd version even worked with growl to pop up info about the test success or failure.

I still have the [Stakeout-2 tarball](http://michael-mccracken.net/software/stakeout-2.tgz) available, but I haven't tested it in years.

Why? I've been working on things that take too long to test, so I don't want to run a suite every time a file changes anymore. I still think it's a useful idea.
