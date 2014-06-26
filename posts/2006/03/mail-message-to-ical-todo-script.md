<!--
.. title: Mail message to iCal Todo script
.. date: 2006/03/03 00:31
.. slug: mail-message-to-ical-todo-script
.. link:
.. description:
.. tags: mac
-->


After reading Merlin Mann's [suggestion to live in iCal](http://www.43folders.com/2006/02/27/contexts/), I thought that even though I don't use [kGTD](http://www.kinkless.com/), it might be a good idea to try to limit the number of places where things I have to do exist. Following on the idea of moving lines of text from [VoodooPad to iCal todos](http://michael-mccracken.net/wp/?p=28), I just wrote a script to take the frontmost email message and add a todo that reminds me to reply to it. I'm getting a little closer to just having one place I need to check tasks.


    
    
    tell application "Mail"
    	set l to the selection as list
    	set selMesg to item 1 of l
    	set cont to content of selMesg as string
    	set subj to subject of selMesg as string
    	set person to sender of selMesg as string
    	tell application "iCal"
    		set theCal to (first calendar whose title is "Email")
    		set theString to "reply to " & person & " about " & subj
    		make todo at end of todos of theCal with properties {priority:0, summary:theString}
    	end tell
    end tell
    



This ends up with a todo that says something like **"reply to michael_mccracken@mac.com about Locations for the party of the century"**

Of course, it's best invoked with a twitch and [Quicksilver](http://quicksilver.blacktree.com), so just drop it in `~/Library/Scripts` so it gets indexed. I called it "NewTodoFromEmail" and Quicksilver calls it "nte". Clever.

I based it on my [NewEventFromEmail script](http://michael-mccracken.net/blog/blosxom.pl/computers/mac/programming/ASiCal.html), which I still use regularly. So nice!
