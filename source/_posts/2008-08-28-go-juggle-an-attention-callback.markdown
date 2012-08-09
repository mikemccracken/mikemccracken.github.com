---
comments: true
date: 2008-08-28 19:31:05
layout: post
slug: go-juggle-an-attention-callback
title: go juggle — an attention callback
wordpress_id: 119
categories:
- computers
- productivity
- scripts
- X Windows
tags:
- script utility productivity
---

Sometimes progress on a project for me consists of a few short bursts of activity in between stretches of waiting for some long-running thing to complete so I can figure out what I need to do with it next.

Because I always have more than one project going, I don't actually wait much. I just switch workspaces and try to make progress on the next thing. If I can't make progress on anything immediate, I'll end up checking email or looking up something for a side project.

This kind of multitasking is inefficient, but inevitable when I might have to wait for 20 minutes or more for a compute job or a compile to finish.

The problem with this approach is that the things I'm waiting for often finish while I'm off doing something else, and if I get too involved, the low-priority research or emails will eat up my day while the high-priority work sits waiting for me.

I've attacked this problem in the past when using OS X with [growl](gr), but I can't call growlnotify from remote systems. However, I just found [dzen](dzen) for X Windows, a lightweight notification display utility that compiles easily on every system I've tried, and works remotely with ssh X forwarding.

I wrote a simple script called `go`, which just executes its arguments and runs `dzen` when it's done. Now I type (for example) `go make` and I can switch over to something else, confident that I'll see a big popup window letting me know when I can get back to working on my highest priority project.

Here's basically the entire `go` script:


    
    
    #!/bin/ksh
    echo $@
    $@
    echo $@ completed on `hostname` \
     | dzen2 -p -h 64 -bg darkblue
    
    



It's simple but it's working great for me. I've tried some improvements like randomizing window placement to avoid overlapping notifications, but the simple version above really does all I need.

Finally, a couple of details. zsh always seems to want to spell-check 'go', so I really named it '~/bin/executeAndNotify.sh' and just aliased 'go' to that.
Also, I've found it can mess with shell quoting as is, so sometimes I have to do `'somecommand ; go echo done'`. If someone has a tip on getting the quoting right in the script, I'd love to hear it. The problem crops up when you try something like 'go make CC="cc -g"' - the quotes don't make it through.

[gr]:http://growl.info
[dzen]:http://gotmor.googlepages.com/dzen
