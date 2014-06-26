<!--
.. title: Handling Reference Emails
.. date: 2011/04/26 09:44
.. slug: handling-reference-emails
.. link:
.. description:
.. tags: email, apple-mail, email, gmail, mikechecksmail, postbox, thunderbird, thunderbird-3
-->


Sometimes you need to refer to your email. (I've written about this [before](http://michael-mccracken.net/2007/06/the-read-once-email-client-and-reference-emails/)).

Maybe it's to integrate comments from a bunch of people while you're editing a report, or it's a set of mails with instructions for something, like how to configure & install a source code package or submit expense reports in the new system. These emails could all be in one thread, but just as often it's a few mails spread throughout several threads and scattered in time.

A good mail client should make it easy to keep arbitrary groups of messages visible for reference. Since they're reference emails, you're just reading them, and the display shouldn't really be more than the text of the mail. You should be able to fit a few of these on screen without overlapping what you're actually working on, and you don't need a big toolbar with a bunch of actions that won't be happening.

When I'm doing something in another app, I want to arrange my reference mails in an empty part of the screen, then not click back over to the mail client until I'm ready to close them. The faster it is to set up this display and get on with things, the better. 

Let's look at how a few existing clients support this kind of thing:

### Gmail

It's easy to open a conversation and refer to it, and you can hide the body of messages that aren't relevant. But you can't move things around, so if it's a really long thread, you might be in for some scrolling. If you want to refer to more than one thread, you will have to open each in its own window.

### Apple Mail

Because of its lack of a conversation-style thread view, the way to do this is to just open separate windows for each message. You can't look at a single thread in one window - have to open N windows for N messages. Ugh.

Since Mail is what I use most often, when I have this problem I always end up with a flock of windows, and lots of clicking, scrolling and cmd-tabbing around to see what I need, followed by looking at all my open windows and trying not to close any unrelated drafts or accidentally send or delete something important.

### Postbox & Thunderbird

The experience with Postbox is similar to, but a little worse than GMail.
In Postbox, there's a thread view where I can hide uninteresting messages like GMail, but if I want to pop the thread out into a separate window, I can't - only single messages can be popped into separate windows. I can make tabs with the thread view by double-clicking on a thread, but I can't figure out how to get a new window. Of course, if I need to see multiple emails at once, tabs are no good.

Thunderbird is basically the same, except at least in 3.0.4, the default view when you select a thread is less useful than Postbox's - it looks more like a debug dump of the message's text than a well-designed display. 

### MailMate

MailMate is similar to Postbox & Thunderbird - except that you get a nice linear conversation-style view with any selection, not just a single thread. (Postbox has a nice view but only for a thread, and TBird shows you any selection but not a nice view.)

Still, as with those others, the linear conversation view can't be popped into its own reading-oriented window, and it's strictly linear.

### Summary

I don't think any of the clients I looked at have a good solution for this. Is that a problem? Is this actually important? 

I think so. I bet if you think about when you actually look at an email, it's usually one of three times - when you first read it, as you write a reply to it, and when you're searching for it later. In both of the second two cases, I've found that I often have more than one mail or thread that I want to look at while I write or do something in another app, and a dedicated view to support that would be great. I could search through just those messages. I could minimize or move them all at once. Just think of the possibilities!

Finally, if it's easy to keep this set of emails around for later reference without cluttering up my screen in the meantime - and without actually moving the messages into some separate folder on my server - that'd be really great. Because you always have another expense report to file, and really, who wants to memorize *that* procedure?

Thanks for reading this far, and please feel free to leave a comment - am I missing something great in one of these clients?
