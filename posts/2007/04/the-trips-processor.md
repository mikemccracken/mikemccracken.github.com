<!--
.. title: The TRIPS processor
.. date: 2007/04/25 11:01
.. slug: the-trips-processor
.. link:
.. description:
.. tags: compilers, computers, HPC, research
-->


The UT-Austin [TRIPS project](http://www.cs.utexas.edu/~trips/) will be unveiling their new processor next Monday. ([event details](http://oea.cs.utexas.edu/articles/index2007/trips_unveiling07.html))

This is a pretty interesting attempt to get around the problems facing processor design today. Clock speeds have stalled, but the actual Moore's Law - the one about transistor count, not "speed" - is still going, so we have the problem of what to do with just a lot of copies of basically the same old chip?

A lot of answers you hear involve pushing that complexity up to the programmer, forcing more people to become parallel programmers. This is almost certain to happen at least a little, but let's hope we don't have to give up on the sequential programming model completely. If you think software is bad now…

The TRIPS processor is an example of another approach - placing more of the burden of finding and using parallelism onto the compiler and architecture, keeping programmers' heads above water. It's pretty exciting to see something this different make its way into actual silicon.

The basic idea is that instead of a single piece of control logic organizing the actions of multiple functional units, finding concurrency within a window of instructions using reordering, the TRIPS processor is distributed at the lowest level - each functional unit is a mini-processor (called a tile), and instructions executing on separate processor tiles communicate operands directly, not through a register file. Usually this is described as executing a graph of instructions instead of a single instruction at a time.

Current processors certainly don't just execute one instruction at a time, and they do plenty of moving instructions around, so I tend to see this explicit-data-graph description as just the far end of a spectrum that starts with old superscalar designs, continues through out-of-order processors and multithreaded architectures, and currently seems to end here.

A TRIPS processor can run four thread contexts at once, with an instruction window of 1024 instructions to reorder and 256 memory operations in flight at once. For comparison, the late '90s Tera MTA ran 128 threads at once (128 different program counters), and the 2003-vintage Cray X1 processors kept track of 512 memory operations at once. Just like TRIPS, each of those architectures required extensive compiler support for good performance.

A particularly interesting point is the fully partitioned L1 cache - meaning that there are multiple distributed L1 caches on the chip, so where your instructions are physically executing will be important for performance - if they're near the cache bank holding their operands, they will execute sooner.

The natural question when looking at a new and interesting architecture like this, especially one that promises a tera-op on a chip, is whether it will make its way to a laptop you can buy anytime soon. I have no idea if the UT team has any industry deals in the works, but I would bet against something like this becoming mainstream quickly - the fact that these architectures rely so much on a custom compiler with aggressive optimization means that a lot of dirty work is required to move existing software to it.

It will be interesting to follow this project and see how their actual hardware performs.
