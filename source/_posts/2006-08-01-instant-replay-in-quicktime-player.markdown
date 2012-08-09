---
comments: true
date: 2006-08-01 13:12:07
layout: post
slug: instant-replay-in-quicktime-player
title: Instant replay in QuickTime Player
wordpress_id: 55
categories:
- hpc
- mac
- programming
---

A feature I really miss from having a DVR is the '8 seconds back' button, to catch a play or repeat something funny.

Recently I've been listening to recorded interviews we've been doing of HPC developers, and updating my notes (in [VoodooPad](http://voodoopad.com/) using them. Since people mumble and use jargon I don't always understand, I decided I really needed an instant replay button in QuickTime Player. It'll come in handy if I watch sports on my laptop again, too.

In order to get it, I wrote this quick AppleScript and bound it to a [Quicksilver trigger](http://docs.blacktree.com/quicksilver/qstriggersprefpane?s=trigger). If you run it while the movie is playing, it backs up 4 seconds and keeps playing from there.


    
    
    -- 4secondsback.scpt
    tell application "QuickTime Player"
    	set theMovie to movie 1
    
    	set ctime to current time of theMovie
    	set tscale to time scale of theMovie
    
    	set current time of theMovie to ctime - (4 * tscale)
    end tell
    



Update: I just realized that for transcribing interviews I also needed a 'play/pause' command that could control QuickTime Player while keeping it in the background, just as the 4secondsback script does. It's a really simple script, but since QuickTime Player lacks the convenient 'playpause' command that iTunes's scripting dictionary has, I had to do this:


    
    
    tell application "QuickTime Player"
    	if movie 1 is playing then
    		pause movie 1
    	else
    		play movie 1
    	end if
    end tell
    



I have this set as a trigger for Control-Option-Space, and the 4secondsback script is control-option-'b'. This way I can listen, type, and control the recordings without leaving VoodooPad. Brilliant!
