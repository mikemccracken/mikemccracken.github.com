---
comments: true
date: 2006-08-28 19:55:45
layout: post
slug: autofill-bibdesk-and-dc-html
title: 'AutoFill: BibDesk and DC-HTML'
wordpress_id: 63
categories:
- bibdesk
- bibliography
- mac
- metadata
- programming
---

For my first contribution to [BibDesk](http://bibdesk.sf.net) in a while, I've added the ability to read Dublin Core metadata when it is encoded in HTML META tags on a web page.

What this means is that when using the "New Publications from Web" feature, some sites you browse to will have the publication's information filled in for you, so you don't have to type anything at all. The [Eprints.org](http://www.eprints.org/) open archive software does this, so check out their [list of archives](http://www.eprints.org/software/archives/) for examples to test it out on.

It'll be in the next version, which isn't scheduled yet, so if you'd like to try it out sooner, see the [nightly builds][nb] page and heed its warnings.

If you publish web sites with one-page-per-pubcation and want info about embedding DC terms in your meta tags, see the [Dublin Core recommendation][dchtml].

If you want to support AutoFill for a site that doesn't have one page per publication, or would like to provide more metadata, I suggest waiting for the [citation microformat](http://microformats.org/wiki/citation). Feel free to ask why...

*Update*: I made a 12-second movie of how it works - [BibDesk, EPrints and Dublin Core](http://michael-mccracken.net/img/BibDesk-DCHTML-screencast.mov)

[dchtml]:http://dublincore.org/documents/dcq-html/
[nb]:http://bibdesk.demokratia.org/beta/
