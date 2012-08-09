---
comments: true
date: 2006-02-03 15:33:09
layout: post
slug: talk-bart-miller-and-dyninst
title: 'Talk: Bart Miller and Dyninst'
wordpress_id: 19
categories:
- grad-school
- programming
- research
---

In a recent largescale systems seminar*, we had [Bart Miller](http://www.cs.wisc.edu/~bart/) from [Wisconsin](http://www.cs.wisc.edu/) talk about some of the upcoming work on [DynInst](http://www.dyninst.org). DynInst is an API for runtime code patching, which lets you do things like attach to a running program and insert your own code around every network call, or replace procedures with your own versions. You can even do something as insane as calling a function every time the instrumented program accesses memory. (We do roughly that here at [PMaC](http://www.sdsc.edu/PMaC/) with [MetaSim](http://www.sdsc.edu/PMaC/MetaSim/metasim.html).)

Bart talked about some of the challenges they've had to face with DynInst and the directions they're planning to take it in the future. The major news is that they're planning to improve support for binary rewriting, in which you use the same interface to instrument an object file and produce a new executable instead of just doing it in memory. Also, they are planning on breaking it up into a few smaller libraries so you don't have to link everything in if you're building a tool that doesn't need all of DynInst. These are both good news for users.

He discussed some interesting applications of DynInst (such as trapping and removing calls to license checking code), and some odd situations that have driven development, like users who needed to instrument binaries that were hundreds of megabytes large (not with linked libraries, just the one file). He also highlighted some cases where DynInst really shines, such as needing to instrument a program that you can't even relink, due to lack of source code access or simple overwhelming makefile confusion. The facility for removing instrumentation led to a clever code coverage tool that removed instrumentation on a block after the block was touched once, leading to a really impressive speedup.

They've also used it to observe viruses without allowing them to write to disk, including nifty tricks like waiting until the virus uncompresses itself, then saving the uncompressed virus for later analysis. The extensive work they've done on binary analysis is important here, because viruses don't really come with symbol tables for handy debugging.

I thought that the most interesting part of the talk was about the challenges they've addressed through the course of the project. For instance, it is surprising how often with production compilers, that the symbol tables contain entries which are totally bogus. An example he used was that the function size information in most symbol tables is never right. Few tools pay attention to this, so it goes unfixed. One reason for this inaccuracy is another reason to consider using DynInst or something like it to build program analysis tools - object code layout is getting pretty confusing, and they've done the hard work of analysis already. For instance, noncontiguous functions are common. Apparently that's rampant in Microsoft's products, due to optimizations that reorder hot basic-blocks. Other weird code arrangements are common, including functions sharing object code. Compilers sometimes appear to be active adversaries to program analysis tools, and many tools in common use are making assumptions about code layout that are increasingly less likely to be correct.

I asked how symbol table information needs to be improved to let tools keep up, and what more information one needs to get from the compiler, and his response was that expecting many-to-many relationships for mapping code to source is very important if your tools need to deal with real code.

Thanks to Bart Miller for the talk - any errors above are mine, the ideas and hard work described are all theirs!

*I had wanted to post about it right away, but I didn't get to it until two weeks later.
