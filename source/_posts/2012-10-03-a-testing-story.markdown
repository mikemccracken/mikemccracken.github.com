---
layout: post
title: "A Testing Story"
date: 2012-10-03 11:37
comments: true
categories: testing
---

Tests are great! This year I've started working on a codebase with a
significant unit test suite for the first time in a while, and good
coverage has definitely come in handy. Now I'm going to share a 
story where a single test did double duty.

Our filesystem events listening daemon was crashing occasionally on my
system, and I didn't know how to reproduce it. No one else seemed to
be getting these crashes, either. The system was saving a backtrace,
and it was always the same, but I wasn't sure I believed its line
numbers. As a start, I made a guess at the lines that were really
failing, and added a ton of debug dumps to inspect the state. (Since
this daemon is run as root using launchd, it's still easiest to just
use the old printf-n'-stare debug method.)

Then I tried a lot of stuff to poke at it, even leaving Spotify on
overnight in an attempt to recreate the conditions of the bug. No
luck. It seemed like it would only crash when I wasn't trying to get
it to crash - pretty frustrating.

I finally found it, but only after giving up for a while. I checked in
again after working for a while on another project, and hey, lots of
new crashes! With all my extra debug info, I could see what was going
on - a string that couldn't be encoded in UTF-8 was being handled by
some code that assumed it could be. It was a filesystem path with
invalid characters.

What was the path that was killing my daemon? It was a temp file written
by the test suite for the other project. It was a non-utf8 path,
written to test the unicode handling of the GUI, and it had the
wonderful (in retrospect) side effect of poking a bug in the daemon
too. It's so satisfying when you find a bug's cause and it completely explains all the symptoms you were seeing.

One test exercising the unicode handling of multiple projects, now that's coverage!