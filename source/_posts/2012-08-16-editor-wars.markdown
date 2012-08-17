---
layout: post
title: "'Editor Wars'"
date: 2012-08-16 23:44
comments: true
categories: programming editors
---

An idea I'd like to see: Editor Wars, the game of hacking at code.

Hackers compete on how fast they can complete code editing tasks from
a variety of languages, with results plotted and dissected on a 
web leaderboard. The idea is not to evaluate language understanding or
design, but simply editing skill and speed in the kind of thing that
editor flame wars start over. 

The tasks could be simple refactorings, like renaming a function
throughout a source tree, or extracting code into a method. I'd expect
this would show advantages of specialized refactoring tools in some
IDEs. Other tasks might be more complex, like writing a new set of
functions, a whole class, or adding functions to a class to conform to
a protocol or interface. Good template support and autocomplete might
be an advantage here. Or maybe you want to add conditional debug
logging around a set of functions, with each call having a separate
hardcoded counter value? Surely powerful macros win this task?
Naturally, new tasks could be submitted by the public, and voted on.
Each task would have a "correct" answer, but if you're really clever
you could always suggest a better correct answer.

Use of extensions and custom macros would be happily encouraged, as
long as you can share what you've used. 

You'd need either an editor plugin or at least something that watches
files efficiently to get the split-second timing your contestants will
demand. Ideally you'd be able to record keystrokes and grab the source
for any macros you call, then the site would be able to show a replay
for the viewing public.

It'd be fascinating to learn how other people use your favorite editor
by watching the best of the best compete. Not to mention, just imagine
the forum threads arguing over the graphs from the vast database of
editor timings.

Anyone want to build this?