---
comments: true
date: 2011-07-06 14:05:48
layout: post
slug: voodoopad-omnifocus-and-terminal-integration-wish-list
title: VoodooPad, OmniFocus and Terminal Integration Wish List
wordpress_id: 493
categories:
- productivity
- tips
---

Here are some features I want but I'll never have time to write the scripts for VoodooPad to do.

I use VP mostly as a running log of notes, shell commands and todos. I also use OmniFocus for task tracking, but sometimes it's easier to just start typing in VP and work out the tasks later. So I often end up with VP pages that have a bunch of todos mixed in with project headers and miscellaneous notes.

I've been thinking some integration would be nice. I want an <del>[emacs org-mode][om]</del> (update: I meant [notes-mode][nm]) style "new day" script that creates a new page for the day and does the following:

* adds a link to the new page to the previous note page
* moves any pending todos (I mark them as lines starting with a <# todo #> placeholder so I can jump to them) off yesterday's page and into OmniFocus 
* starts a new header (line starting with #, in bold) in the new page for every header that had leftover todos. These headers usually correspond to projects in OmniFocus.
* adds new headers and todo lines for any tasks that are due today

I want to have VP autocomplete project names from OmniFocus when I start a header line. Then add a link next to the new header pointing to the last page containing that header. 

I'd also like to have OmniFocus update the VP document when I check off a task in OF - I want to use VP as a log, so I can track down when I did something. Maybe projects should all have their own VP pages, that are kind of an auto-updated index of progress on the tasks.

It'd also be nice if when I edited a todo line in VP, it could update OF. I guess I want VP to be an supplemental synchronized view onto my OF tasks.

For the Terminal: I do a lot of copying and pasting shell commands into VP so I can remember things like important paths, or the exact configure settings I used to build something two years ago. This is really useful, but it'd be nice if it was easier to do without leaving the terminal. Ideally I could just prefix a command with something like '@' to add it to the current page in VP (or '@pagename#headername' to get fancy). You could get this with a script named '@' - on your local machine. But it also has to work when you're working remotely, so it will get a little more complicated.

Finally - this is something I wanted to try doing with an InputManager before that mechanism went away: I'd like CamelCase links in every text field on the system (probably with some exceptions) to automatically link to VP pages. But it sounds like the days of modifying system-wide behavior on Macs are history, so I'll probably never get this. Who knows, maybe it would've been a disaster. 

I always thought the path to improvement in work computing was more and deeper integration between 3rd-party apps, as well as more system functionality that's usable by all those apps, but it looks to me* like in OS X we're only getting the latter.

_* - since 10.7 is about to come out, it might be worth pointing out that I have no special advance developer info. I haven't even been a dev program member for a few years now._
[om]:http://orgmode.org/
[nm]:http://www.isi.edu/~johnh/SOFTWARE/NOTES_MODE/
