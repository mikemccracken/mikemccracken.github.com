---
comments: false
date: 2010-05-28 06:00:00
layout: post
slug: filters-thunderbird-3
title: 'Filters: Thunderbird 3'
wordpress_id: 325
post_format:
- Aside
tags:
- filters
- lists
- thunderbird-3
---

How well does Thunderbird 3 let me create filters to handle heavy traffic lists?

There's not much support for using a message to build a filter from, which I think is the most natural workflow. The menu item "Tools > Message Filters…" opens a dialog box that could use some simplification. For example, the buttons to move filters up and down in order are unnecessary - you should be able to just drag the filters around in the table. There are plenty of other non-mac-like UI elements here. Another example of overcomplicated UI is the "Filter Log" button. At best this is an "advanced" preference, but it's a big button at the top - and it's misnamed. It opens a sheet to let you turn the logging on, but who knows how you actually view the logging?

![](http://media.tumblr.com/tumblr_l33l1uJlv51qz505e.png)

There are some other UI problems when trying to add the filter - I didn't think ahead of time that I'd need to create the folder to send the filtered messages to. The Message Filters dialog seems modal, because the menubar goes away when it's in focus, but it's not really - so I just created the new folder back on the main window while the new-filter sheet was still open. A little strange, but it worked.

It's also lacking a way to do a dry-run of the filter- to test which messages will match, before just letting it loose on your mailbox. This is a really important feature, especially when filters can do destructive or un-recoverable things like running a script (not in Thunderbird, but present in other mailers) or send a response.
