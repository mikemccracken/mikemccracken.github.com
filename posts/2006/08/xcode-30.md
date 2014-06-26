<!--
.. title: XCode 3.0
.. date: 2006/08/07 23:27
.. slug: xcode-30
.. link:
.. description:
.. tags: computers, programming, wwdc
-->


Apple's [XCode 3.0 preview page](http://www.apple.com/macosx/leopard/xcode.html) is a cornucopia of new stuff that I somehow missed all day - until now.

No doubt this is the stuff that everyone at WWDC is talking about. This page represents no less than 3 or 4 really significant changes and some really nice details. Here's a hit list that I haven't seen in any of the coverage I've been looking at today:

 * **Garbage Collection** in ObjC. I'm curious about the details, but I'm also certain that it's a good thing. I really just think this is a no-brainer and we'll all be asking how we lived without it in a year.

 * **Project Snapshots** - lets you fiddle with projects and go back to a good state without involving SVN. Nice, it's like Word Versions for XCode. Handy, but a little puzzling why it seems to be duplicating version control functionality.

 * **Research Assistant** - A 'lightweight window' for reference and API docs. Long overdue, and sounds really handy. Basically what I [asked for](http://michael-mccracken.net/blog/blosxom.pl/2004/07/07) in a Dashboard Widget long ago.

 * **[DTrace](http://www.sun.com/bigadmin/content/dtrace/)** for Mac OS - this is an extremely useful and powerful dynamic tracing framework from Sun - with a [DSL for tracing](http://www.sun.com/software/solaris/howtoguides/dtracehowto.jsp#1) called "D", and I'm really surprised to see it on OS X. This is nice.

 * Leveraging DTrace, **XRay** visualizes program behavior. I think DTrace itself is more interesting, based on my experiences with visualization of parallel program behavior and developers (generally allergic) reaction to it, but it's interesting to see Apple give it a serious try. The ability to "track UI events" sounds tantalizingly useful.

 * A new text editor - apparently it can shade text backgrounds according to scope. This could either be a non-starter or really great. I think some will love it after a while and some will hate it immediately. Which are you? Oh, it also does iChat-style popups on your breakpoints. Okay.

 * Finally, Interface Builder 3.0, where they spend a lot of time talking about some extra palletized stuff you can drop in, which is all well and good, but then they drop the boom in the last two sentences: ***"Interface Builder 3.0 makes localization and diffing easier. And you can include your NIBs in global refactoring tasks."*** Whoa! That sound you just heard? [It was me from 2004](http://michael-mccracken.net/blog/blosxom.pl/2004/07/07), cheering them on.


 **Update**: `s/XCode/Xcode/` - thanks.
