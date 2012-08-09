---
comments: true
date: 2006-01-26 17:39:34
layout: post
slug: pldi-papers-im-interested-in-part-one
title: PLDI Papers I'm interested in, part one
wordpress_id: 16
categories:
- compilers
- grad-school
- research
---

I mentioned that I'd post about some of the papers I found interesting from this year's PLDI conference. Disclaimer: for the most part this is based on reading the abstracts only, so this shouldn't be considered a thorough review.

Session one is Transactions. I will probably look through these, especially the first paper, *"The Atomos Transactional Programming Language"* [1] from Stanford, because transactional memory and processing seems to be a consensus pick for the next big thing, and [Burton Smith](http://www.computerhistory.org/events/lectures/smith_01232001/) once told me that languages using transactional memory and invariants with respect to state are his bet for what can solve the parallel programming problem. (What problem? It's too hard to write good parallel code.) So, I want to see what a transactional language looks like.

There's a paper in the Compilers session that looks like a cool idea for improving analysis - *"A Framework for Unrestricted Whole-Program Optimization"* [2]. The [abstract](http://liberty.princeton.edu/Publications/index.php?abs=1&setselect;=pldi06_pbe) says they have a way for intra-procedural passes to work on arbitrary subgraphs of the program, so they're not just limited by procedural boundaries, and don't have to rely on inlining to optimize across calls. I'm curious what languages it supports, and how the scheme would work with dynamic languages.

A paper about dynamic software updating, *"Practical Dynamic Software updating for C"* [3] ([project link](http://www.cs.umd.edu/projects/dsu/)) is also interesting, because it seems like a step towards the way things should work. Essentially, they compile a program so that it can be easily updated without stopping it. They do it in a way that doesn't violate type-safety and sounds reasonably efficient. It reminds me of Apple's ZeroLink and Fix & Continue (note that those aren't the first examples of such technology), and I'm curious how similar it is. Certainly I don't think Fix & Continue tries to guarantee type-safety.

The parallelism session should be interesting, and I'm most curious to see an abstract for *"Shared Memory Programming for Large Scale Machines"* [4], I can't tell from the title if they are introducing a new language or measuring an existing technique. I have a note to myself somewhere to look for a full copy of that paper.

Power has been a big deal in HPC and mobile devices for a while, and now it's everyone's problem, so *"Reducing NoC Energy Consumption Through Compiler-Directed Channel Voltage Scaling"* [5] caught my eye. I'm always interested to learn about power usage effects of different kinds of code, since I have found it to be satisfyingly unintuitive at times. (Maybe I should've taken more EE classes!) Also, this is a paper from Penn State, and I'm curious what research they've got going on back at my alma mater.

I'll probably read everything in the Runtime Optimization and Profiling session, but *"Online Performance Auditing: Using Hot Optimizations Without Getting Burned"* [6] is particularly interesting, since I know Brad Calder and his students do really good work, and I honestly didn't know what Jeremy was up to. I should probably be more social around the department. (These guys are at UCSD)

OK, I'm not out of interesting papers, but I'm going to stop here for now. Check out the program, let me know what you think is cool - am I missing something really great?

####References


[1] "The Atomos Transactional Programming Language"
Brian D. Carlstrom, JaeWoong Chung, Austen McDonald, Hassan Chafi,
Christos Kozyrakis and Kunle Olukotun.

[2] "A Framework for Unrestricted Whole-Program Optimization"
Spyridon Triantafyllis, Matthew J. Bridges, Easwaran Raman, Guilherme Ottoni, and David I. August

[3] "Practical Dynamic Software Updating for C"
Iulian Neamtiu, Michael Hicks, Gareth Stoyle and Manuel Oriol

[4] "Shared Memory Programming for Large Scale Machines"
Christopher Barton, Calin Cascaval, Siddhartha Chatterjee, George Almasi, Yili Zheng, Montse Farreras, Jose Amaral

[5] "Reducing NoC Energy Consumption Through Compiler-Directed Channel Voltage Scaling"
Guangyu Chen, Feihui Li, Mahmut Kandemir, Mary Irwin

[6] "Online Performance Auditing: Using Hot Optimizations Without Getting Burned"
Jeremy Lau, Matthew Arnold, Michael Hind, Brad Calder
