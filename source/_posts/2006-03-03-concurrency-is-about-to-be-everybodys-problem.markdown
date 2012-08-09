---
comments: true
date: 2006-03-03 01:30:54
layout: post
slug: concurrency-is-about-to-be-everybodys-problem
title: Concurrency is about to be everybody's problem
wordpress_id: 32
categories:
- computers
- research
---

[Herb Sutter](http://www.gotw.ca/), software architect at Microsoft, chair of the ISO C/C++ committee, and [blogger](http://pluralsight.com/blogs/hsutter/), gave a talk this Monday about the impending concurrency revolution and his project, Concur, an extension to C style languages to support usable concurrent programming. I enjoyed his talk in spite of the job-fair atmosphere (it was also a Microsoft recruiting event) and having to stand the whole time, so I'd say it was a good talk.

Check out his article ["The Free Lunch is Over"](http://www.gotw.ca/publications/concurrency-ddj.htm) for a programmer's viewpoint on what to do with the processors we're currently faced with. This is a very exciting time for computing - parallelism has always been the future, and the future is finally now. I am increasingly convinced that as a programmer, if you resist learning how to program concurrent systems, then you will be obsolete very, very soon.

The reason is that processor architects have density to waste, but they have nearly run out of ways to use extra transistors to make single processors faster - so they're happily just shipping chips with bunches of smaller processors. According to intel's (nicely readable) [Platform 2015](http://www.intel.com/technology/architecture/platform2015/) site, Dual and Quad-core isn't nearly the end - today's college freshman will likely start out their career programming not "multi-", but "many-core" systems (think 'at least hundreds'), requiring hundreds or thousands of independent threads of execution to avoid leaving performance on the table. Are we preparing students for this? I doubt it.

So, should we all run off and learn all about pthreads and mutexes? No - concurrent programming is really hard, even to get it almost right on a toy problem. In some areas (like servers and mathematics used for scientific computing), concurrency is a "well-understood" problem, but even there it's widely understood to be hard. No wonder everybody's been avoiding it.

This is really a problem for language designers, framework designers, and compiler writers - how do we build an environment where a reasonably competent developer can write and debug programs with a very high level of concurrency? For everyone else, just keep your eyes peeled - [they're working on it](http://www.cs.purdue.edu/homes/jv/events/TRANSACT/).

To quote Maurice Herlihy, from an invited speech ([ppt slides](http://research.ihost.com/pldi2005/manifesto.pldi.ppt)) at 2005's [PLDI](http://www.acm.org/sigs/sigplan/pldi.htm) conference (for compiler writers and language jockeys), This situation amounts to a "PLDI Full-employment act". Interesting times, indeed!
