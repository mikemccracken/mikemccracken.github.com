---
comments: true
date: 2008-01-13 13:58:55
layout: post
slug: what-is-site-reliability-engineering-at-google
title: What is Site Reliability Engineering at Google
wordpress_id: 114
categories:
- computers
---

I've been looking around for some more detailed information about the "Site Reliability Engineering" positions at Google.
Apparently the role is a real mix of very large-scale system administration, planning and automation.

I've collected some links to public info about the job.

The Google channel has [a promotional video](http://www.youtube.com/watch?v=y31STIrwtlk) from one engineer about the role - he tells a quick story about being on call to monitor and address problems with Google talk.

A set of [slides from a talk by James Youngman](http://www.ukuug.org/events/spring2007/programme/ThatCouldntHappenToUs.pdf) at the UK Unix & Open Systems User's Group gives a good description of the general task, and dives deeper into two specific examples - powering down failed disks, and protecting data with checksums, exploring how straightforward ideas can explode at scale.
(These slides also have potentially the best proprietary-information disclaimer I've ever seen: "This has been written entirely in ASCII. No EBCDIC or animal fat.")

[Here](http://sysadmin.miniconf.org/2006/pollmann_google_lightning_talk.ppt) is another set of slides with a quick overview, from a 'lightning talk'.

A sampling of what Google SRE engineers put in their public resumes about their job includes quite a span - from troubleshooting mission critical services to writing automation software (in Python).

And finally, an [interesting post from 2006](http://googleresearch.blogspot.com/2006/03/hiring-lake-wobegon-strategy.html) about the theory behind Google's hiring strategy, summarized as "only hire candidates who are above the mean of your current employees".
