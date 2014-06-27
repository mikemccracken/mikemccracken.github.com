<!--
.. title: TextShapeView
.. date: 2009/09/17 12:49
.. slug: textshapeview
.. link:
.. description:
.. tags: cocoa, mac, NSTextView, text
-->


TextShapeView was another Cocoa Text system hack project I started a few years ago.

I made a view that displays a zoomed out view of a string from a text view, with indentation, along with a rectangle showing where the text view is in the file. 

You can click around in the view to move the  It also highlights the selection, and draws lines in blue if they contain the string in the NSFindPBoard, so you can see *all* the lines in the file that match when you use the Find panel.

This is available under a Creative Commons license, and I'd ask that if you make any improvements, you send them back to me or join the 'leverage' sourceforge project, where the code is hosted. I wanted to eventually make this into a Cocoa text plugin like [my I-Search plugin](http://michael-mccracken.net/2009/09/an-update-on-the-incremental-search-plug/).

Here is the [SVN repository for the textshape code](http://leverage.svn.sourceforge.net/viewvc/leverage/textshape/trunk/).

There was also a [Source code Tarball](http://michael-mccracken.net/TextShapeView.tgz) with a demo app, shown in the screenshot below:

[![](http://michael-mccracken.net/img/tsvPic.png)](http://michael-mccracken.net/img/tsvPic.png)

