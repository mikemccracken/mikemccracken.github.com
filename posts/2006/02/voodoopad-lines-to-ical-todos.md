<!--
.. title: Voodoopad lines to iCal todos
.. date: 2006/02/27 23:51
.. slug: voodoopad-lines-to-ical-todos
.. link:
.. description:
.. tags: mac
-->


I take notes at meetings in VoodooPad, and as such I write a lot of to-do items in MeetingNotes pages. They tend to get buried in those pages unless I do something about it fast. Sometimes I put them somewhere more useful, like on my "TodoToday" page, but that page is getting more like a "TodoSomeday" page, and isn't fit for serious action items. Today I realized that I wanted a script to take line-items from VoodooPad pages and make them into Todo items in iCal, so I can track them easier.


I already have a [Quicksilver plugin for creating new todos](http://michael-mccracken.net/blog/blosxom.pl/computers/mac/todoQuickSilver.html), so I repurposed it as a python plugin for VoodooPad to add a big list all at once. Check out [Gus' post on python plugins](http://www.gusmueller.com/blog/archives/2006/1/21.html) for the enabler, and then check this sucker out:


    
    
    VPScriptSuperMenuTitle = "Notes"
    VPScriptMenuTitle = 'Create Todos in iCal'
    
    import os
    
    def main(windowController, *args, **kwargs):
    	tv = windowController.textView()
    	s = tv.string()
    	ranges = tv.selectedRanges()
    
    	scriptString = ""
    	for r in ranges:
    		rs = s.substringWithRange_(r.rangeValue())
    
    		lines = rs.split("\n")
    		for line in lines:
    			if len(line) < 1: continue
                scriptString += "tell application \"iCal\"\n\
                set theCal to (first calendar whose title is \"Work\")\n\
                make todo at end of todos of theCal with properties\
                {priority:0, summary:\"%s\"}\n\
                end tell\n" % line
    
    	f = os.popen("/usr/bin/osascript", 'w')
    	f.write(scriptString)
    	f.close()
    



Want to add to it? These and many things are easily imaginable:

* Change priority based on the first character of each line
* handle continuation lines better
* change calendar to select based on some simple syntax, like "* foo" is a line with text "foo" but "*foo bar" is a line with text "bar" destined for calendar "foo"...
* Another idea: a line starting with the words "email" or "mail" be made into a todo with the glyph ✉, and/or an actual email in Mail.app.
* Any other ideas?
