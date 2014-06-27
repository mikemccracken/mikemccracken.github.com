<!--
.. title: Getting notes to work with LaTeX Beamer and Skim
.. date: 2010/04/30 09:34
.. slug: getting-notes-to-work-with-latex-beamer-and-skim
.. link:
.. description:
.. tags: mac
-->


I'm writing a presentation with [Beamer](http://bitbucket.org/rivanvx/beamer/wiki/Home), a LaTeX class for making PDF slides.

There's a built-in way to generate "notes", which was geared towards Acrobat Reader - it basically makes a double-wide PDF page and Reader will show the 'notes' page on the second screen. (I'm guessing it assumes your laptop screen is arranged on the right of your presentation screen, it's the same size or bigger, etc...)

This doesn't work for my personal favorite PDF reader, [Skim](http://skim-app.sf.net) - but luckily there is a full explanation of how to make it work on the [Skim Wiki: Tips and Tricks page](http://sourceforge.net/apps/mediawiki/skim-app/index.php?title=Tips_and_Tricks#Interaction_with_LaTeX_Beamer). The short of it is you create three tex files - one with all the content and two wrappers that generate two versions of the same presentation. One version has slides and the other has notes. Then you can set up Skim to auto-scroll the notes PDF as you move through the slides PDF in presentation mode.

Big thanks to whoever wrote that tip - and to Christiaan for making such a great app.
