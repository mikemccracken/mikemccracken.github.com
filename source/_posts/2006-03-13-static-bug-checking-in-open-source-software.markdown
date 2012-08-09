---
comments: true
date: 2006-03-13 20:00:52
layout: post
slug: static-bug-checking-in-open-source-software
title: Static Bug Checking in Open Source software
wordpress_id: 35
categories:
- programming
- research
---

[Coverity](http://www.coverity.com), the company formed by the people behind the Stanford MC Checker, has started posting regular reports from their analysis tools on prominent open-source projects at [scan.coverity.com](http://www.scan.coverity.com).

I found out about this through [an email from the Coverity CTO](http://gcc.gnu.org/ml/gcc/2006-03/msg00187.html) on the GCC mailing list, and it seems to have been received with some moderate enthusiasm. I think it's a good idea, but as usual the specter of false positives makes the developers itchy, especially when they're publishing bug counts...

[Dawson Engler](http://www.stanford.edu/~engler), the professor at Stanford who was behind all this bug-finding work (and co-founded Coverity) gave a talk recently here at CSE, about newer approaches to finding bugs that uses execution on symbolic inputs - meaning that you mark some inputs to a program as symbolic, and somewhere there's a theorem prover that goes to work finding out if any value of those inputs can cause an error or a crash - then you can run the original code on the input to verify the problem. A nice consequence here is that the generated 'bad' input is then guaranteed to actually be bad, since you can test it and force the error.

There's a paper about that from Engler's group [here](http://www.stanford.edu/~engler/cstr-3.25.5.pdf), and apparently this [PLDI 2005 paper from Bell Labs](http://cm.bell-labs.com/who/god/public_psfiles/pldi2005.pdf) is very similar.

Here's Prof. Engler's slides from [talks about the new work on bug finding](http://www.stanford.edu/~engler/usenix-security05.pdf) and an entertaining
[talk about commercializing the MC Checker](http://www.stanford.edu/~engler/spin05-coverity.pdf).
