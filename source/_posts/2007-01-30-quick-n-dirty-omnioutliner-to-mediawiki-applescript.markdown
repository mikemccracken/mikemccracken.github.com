---
comments: true
date: 2007-01-30 18:42:37
layout: post
slug: quick-n-dirty-omnioutliner-to-mediawiki-applescript
title: Quick n' Dirty OmniOutliner to MediaWiki Applescript
wordpress_id: 86
categories:
- mac
- web
---

The other day, I had a big outline on a wiki that I wanted to edit in [OmniOutliner](http://www.omnigroup.com/applications/omnioutliner/) so I could hide and move things around with a real outliner, then export it back out to the wiki.

I managed to get it into OO with copy and paste and a lot of RSI-inducing tabbing, but the text export options can't be massaged to export MediaWiki-style (eg, '#' for level one, '##' for level two).

So I wrote a quick Applescript to get the data out and get me back on my way. I thought I'd post it in case it would be useful to anyone else:


    
    
    tell front document of application "OmniOutliner Professional"
    
    	set expText to ""
    
    	repeat with aRow in rows
    		set rowText to ""
    		-- start from 2 to treat top levels as headers
    		repeat with i from 2 to level of aRow
    			set rowText to rowText & "#"
    		end repeat
    		set rowText to rowText & " " & topic of aRow
    		set expText to expText & return & rowText
    	end repeat
    
    	set the clipboard to expText
    
    	display dialog "The exported text is in the clipboard."
    end tell
    



Update: see the comments for a version for TWiki. Thanks, Peter!
