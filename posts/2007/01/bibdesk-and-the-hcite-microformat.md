<!--
.. title: BibDesk and the hCite Microformat
.. date: 2007/01/26 07:06
.. slug: bibdesk-and-the-hcite-microformat
.. link:
.. description:
.. tags: bibdesk, bibliography, hcite, metadata, microformats
-->


This is about building an iTunes store-style interface to the web's bibliographic information.

I've been pushing along the [hCite ](http://microformats.org/wiki/citation) Microformat process, which will set a standard for HTML publishers to add simple semantic markup to their pages that programs like BibDesk can read as citation metadata.

In stark contrast to great but complex things like Z39.50, if you can publish a web page, you can serve citation metadata. No need to have servers to support complicated queries, let google do the hard work.

The progress on the standard has been slow, and so far there is only one beta implementation to help focus the talks - Brian Suda's [X2C](http://suda.co.uk/projects/microformats/X2C/) XSL stylesheet.

In the spirit of building momentum, I've added support for parsing hCite to a private build of BibDesk. For now, we're just discussing how to merge it, but soon the feature will show up in nightly builds, and anyone can start testing and getting experience with the emerging standard. I'll update when it's available, but until then, here's a rough screenshot:

![](http://michael-mccracken.net/img/bdwebgroupscreenshot.png)

**Update:** this feature is now in the latest [nightly builds][bdnb], but it's hidden because hCite isn't final. To see the web group, type `defaults write edu.ucsd.cs.mmccrack.bibdesk BDSKShouldShowWebGroup true` (all one line) at the command line before running a recent nightly.

[bdnb]:http://bibdesk.demokratia.org/beta/
