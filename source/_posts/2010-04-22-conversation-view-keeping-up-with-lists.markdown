---
comments: false
date: 2010-04-22 12:57:00
layout: post
slug: conversation-view-keeping-up-with-lists
title: Conversation View & Keeping up with Lists
wordpress_id: 331
post_format:
- Aside
tags:
- apple-mail
- conversation-view
- gmail
- lists
- postbox
- thunderbird
---

Here's a set of screenshots that show how conversation view can help keeping up with a public list.

I've been subscribed to the LLVM-dev mailing list for years in GMail, and for about a week in my mikechecksmail test account. I'm not active in the LLVM project - it's just something I want to check in on occasionally. (For a while I had a filter that popped up any mention of Fortran). So when I check in, I want to skim the threads and read anything that's interesting. Usually that means I'm finding a thread that's already pretty long and I'm reading the whole thread from the beginning the first time I see it.

I'm interested to hear if that's not how you read public high-traffic lists - do you try to keep up with all the threads as they come in? I did that for a while, but it's hard to keep up with and probably isn't actually your job.

So, with that workflow in mind, how do our clients fare?

**GMail**

In GMail, when you click on a new thread (aka "conversation") you get the messages all on one page, starting with the earliest - perfect for reading from the beginning. This shot shows the first couple of messages in a medium size thread:

![](http://media.tumblr.com/tumblr_l1ai4mO4Al1qz505e.png)

It's pretty good about handling quotes, too. If you're reading through an entire thread at a time, it's nice to have quoted text collapsed so you don't end up scrolling past the same paragraphs over and over. Of course, quoted text can be critical for understanding the new text:

    - show quoted text -
    Yes.

    - show quoted text -
    No!!

But in my judgement, barring some natural language analysis, the best default is to collapse and let the user click to expand quotes when necessary.

Finally, if you return to a thread and it has new messages, it'll collapse the ones you've seen before, handy to get a quick update:

![](http://media.tumblr.com/tumblr_l1ajpwBp531qz505e.png)


**Postbox**

If you select "Show Conversations" in the "View" menu, Postbox shows something like a conversation-view when you select an entire thread. If you don't have that option on, or you select more than one message in any other way - like shift-or-command-clicking multiple messages, you get a blank content view. Not very useful, but a minor point - after all, GMail doesn't really show the list in the same page as the content anyway, so they've avoided that design problem.

The major problem with Postbox's conversation view - for this list-catchup task - is that it sorts the messages with the newest ones at the top. This is exactly the wrong thing for reading a whole thread, and I couldn't find a way to change this sort order.

Here's what it looks like on that same thread:

![](http://media.tumblr.com/tumblr_l1ajxnHkKi1qz505e.png)

There are a couple other minor nitpicks - the info pane with the sender and links on the right-hand side only shows its info for the most recent message - if you want that info for another message, you have to select just that message in the list view.

If you revisit the thread, it marks every message as read, and there's no way to see what's new:

![](http://media.tumblr.com/tumblr_l1ajzroxSb1qz505e.png)

If you're still looking at the thread when new messages in that thread come in, it'll give you a nice alert and lets you refresh the view, but then the problem is still there - it's up to you to see what's new.

**Thunderbird**

Thunderbird 3 has a summary view, but it's not thread-centric.
It just shows the sender, date and first few lines (smashed together without newlines) of each message you've selected. If you select a thread, it's kind of like a conversation view, but if you select multiple unrelated messages, it'll just show the messages in order.

Here's what that looks like:

![](http://media.tumblr.com/tumblr_l1ak9yEo0u1qz505e.png)

Clearly there's some room for improvement there. I won't pick on it too much, except to say that smashing the text together for a summary makes this view basically useless.

**Apple Mail**

Apple Mail doesn't really try to give you a summary of a thread or a conversation view - it'll show which mails are new, but then you have to click through to an individual view of each message. Here's what it looks like:

![](http://media.tumblr.com/tumblr_l1akg4XWv41qz505e.png)

This isn't sloppy like Thunderbird's view, but it's not very useful either. For this and other reasons, keeping up with public mailing lists in Apple Mail is pretty painful. That's why I moved most of my list subscriptions over to GMail a few years ago.
