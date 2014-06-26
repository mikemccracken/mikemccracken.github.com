<!--
.. title: SVN in emacs vs. TextMate
.. date: 2009/07/15 07:17
.. slug: svn-in-emacs-vs-textmate
.. link:
.. description:
.. tags: 
-->


Some responses I got to my post about SVN workflow pointed out TextMate's SVN integration. It looks like I could do what I want in TextMate, but it didn't look as smooth as the dedicated clients, and I might be wrong but it gave the impression that I couldn't set it all up without a lot of mousing around. Since I'm an emacs addict, I'm probably not going to give TextMate a real try, but in this case I think there'd be no reason to. I'll explain why.

It's not hard to get the layout I want in emacs with VC-mode. I put a screenshot below. On the left is a window (the whole OS window is an emacs "frame") with dired under VC - the directory edit mode showing what's modified. I've marked two of them so I can commit them together. In the middle I'm viewing the diff for one of the files, and on the right I'm editing the log entry for the entire commit. I can change things around without losing my log message - view other diffs, make edits, etc.

[![SVN in Emacs: Dired under VC / VC-Diff / Log-Edit](http://michael-mccracken.net/wp2/wp-content/uploads/2009/07/emacs-snap-1024x511.png)](http://michael-mccracken.net/wp2/wp-content/uploads/2009/07/emacs-snap.png)

The only real problem I have with this is that it takes a bit of manual window setup every time to get to this arrangement and clean up the diff buffers, and that the display could be nicer. Cornerstone fixes the display issue, and if it (or another SVN client) got the workflow right, it'd fix the first.

I wrote an emacs function once to do that setup automatically. I called it vc-checkin-mike, and it got about 80% of the way there. Enough to feel like I'd spent too much time on it, but not enough that I wanted to use it.

As far as I can tell from screenshots, TextMate is roughly in the same spot as emacs - I can do what I want but it takes a bit of manual setup, and it's not as pretty as the dedicated clients like Cornerstone.
