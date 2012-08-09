---
comments: true
date: 2008-01-02 13:15:15
layout: post
slug: twitter-stats-in-svg-using-gnuplot
title: Twitter Stats in SVG using gnuplot
wordpress_id: 113
categories:
- scripts
- web
---

[Damon Cortesi](http://twitter.com/dacort) just shared a handy script for grabbing your tweets and compiling some stats about when you post to twitter and who you reply to.

His script generates a list of numbers and included a Numbers template to paste them into. Since I don't have Numbers, I've modified [his script](http://dcortesi.com/2007/12/27/twitter-stats/) to write a file that can be read by [gnuplot](http://gnuplot.info), and wrote a basic gnuplot script to output an SVG file version of the stats.

While I was at it, I changed it so it no longer counts "@someone" separately from "@someone:".

Both scripts are right here - [gnuplot_twitterstats.tgz](http://michael-mccracken.net/twitter/gnuplot_twitterstats.tgz)

It uses gnuplot 4.2, which you can get on OS X with [macports](http://www.macports.org/) using `port install gnuplot +no_x11'`. (Or it's a pretty easy build on its own, see the [gnuplot download page](http://gnuplot.sourceforge.net/download.html) )

Here are my stats:
Sorry, it looks like your browser doesn't support SVG. You're really not missing much.
[Click here for a full-screen version.](http://michael-mccracken.net/twitter/2007stats.svg)
