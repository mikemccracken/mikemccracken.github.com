---
comments: true
date: 2010-02-16 23:51:53
layout: post
slug: how-bibdesk-generates-apple-help-and-a-web-manual
title: How BibDesk generates Apple Help and a web manual
wordpress_id: 264
tags:
- apple-help
- bibdesk
- help
- texinfo
---

This is something that had been on my old blog in 2006 and went away, so I'm reposting something I wrote to the macsb list a few years ago:

For the BibDesk open source project, we wanted to have legit in-app
apple help, as well as a web page (and PDF), without maintaining
separate sources, since we were all working out of spare time.

We tried a few free options, and eventually worked out something
decent with Texinfo, a latex-like markup language that can be
processed into latex (and then PDF) or HTML.

I wrote a custom init file to have the (standard) texi2html script
print out apple help compatible HTML. One post-processing script and a
simple xcode script build phase later, and we get apple help.

We also get a version a little more suitable for the web (more content
per page) from the same source: [http://bibdesk.sf.net/manual/](http://bibdesk.sf.net/manual/)

It's worked well for a couple of years, and it's a good choice if you
don't mind learning texinfo (it's pretty nice compared to
writing in Docbook or HTML, IMO), and very good for version-controlled collaboration,
since it's just text.

For an example, here's what the help source text looks like:

http://bibdesk.svn.sourceforge.net/viewvc/bibdesk/trunk/bibdesk/English.lproj/BibDesk%20Help/bibdesk.texi?view=markup

The init file and other stuff is here:
http://bibdesk.svn.sourceforge.net/viewvc/bibdesk/trunk/bibdesk/BibDesk%20Help/

If anyone's curious about it, feel free to ask me questions here. I'll try
to remember how it works.

