---
comments: true
date: 2011-04-05 14:36:25
layout: post
slug: cram-simple-testing-for-shell-programs
title: Cram & Simple testing for shell programs
wordpress_id: 365
categories:
- programming
tags:
- testing
---

[Cram](http://bitheap.org/cram/) is a test framework for command line programs, originally written for mercurial's test suite.

I like the approach - it just reads a shell transcript and runs the commands it finds. If the output doesn't match, it shows you a diff. It's kind of like doctest.

It looks refreshingly simple to get started with, something that so many other test frameworks fail horribly at.

A while ago, I wrote something similar for work. After trying and failing to find a testing framework that wasn't over-engineered, I wrote a script that looks in `./test/ `, and runs every file named `whatever.test`, and compares output to files  `whatever.test.stdout` and  `whatever.test.stderr`, if they exist. 
If not, it just uses the return value to determine success. 

I loved how easy it was to add a test. Just write a script! There is no step two.


(`cram` found via [Titus Brown](http://ivory.idyll.org/blog/mar-11/trying-out-cram) )
