<!--
.. title: Subversion Client Issues
.. date: 2009/07/13 07:17
.. slug: subversion-clients
.. link:
.. description:
.. tags: mac, programming, gui, mac, svn
-->


I use subversion, and won't switch to something newer for a while, so it's worth looking at how to polish that old hammer. I'm used to using the command line svn, or emacs. But recently I decided to try out a few of the nice GUI clients that are around, including [Versions][v], [ZigVersion][z] and [Cornerstone][c].

Of these, the only one that's polished enough to lure me away from emacs and seems to support my favorite mode of working is Cornerstone, and it still gets it a little wrong.

I like to write log comments while looking at (and scrolling through) the diffs for the files I'm committing. This means I want a text field for writing log comments on the same screen as the diffs, that isn't modal, and doesn't stop me from moving around between multiple diffs.

As far as I could tell, I couldn't get the comment field and the diff display shown together in Versions, and while I could in ZigVersion, that app had a subpar diff display and lacked polish overall, missing key shortcuts where I'd expect them, for instance. Cornerstone almost lets me do what I want, but it displays the comment field in a modal sheet, so I have to cancel to change which diff I'm looking at.

This is easy in emacs, but I like a nicer diff GUI. Am I just missing something? This feels like a natural workflow, so it seems strange that no clients support it well.

[v]: http://versionsapp.com/
[c]: http://www.zennaware.com/cornerstone/
[z]: http://zigzig.com/
