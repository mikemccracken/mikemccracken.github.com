<!--
.. title: Mac IRC clients
.. date: 2012/12/13 09:03
.. slug: mac-irc-clients
.. link:
.. description:
.. tags: irc, mac, apps, review
-->


At Canonical, we are spread all over and keep in touch via IRC. I've
tried out a bunch of IRC clients, but nothing is quite right. I'll
explain. Here's a list of some things I want from a client - it's
probably not complete, but it'll do for now:

 1. Don't crash. A bouncer makes crashes recoverable, but I shouldn't
 have to use one just to keep the backlog around.

 2. I need to search the backlog. Incremental search is best.

 3. Show multiple channels at once, in one window.

 4. Highlight mentions of my nick so I can glance at a window and see if anyone's asking me something. Use Growl or notification center, too.

 6. Make it obvious when I've disconnected, and reconnect robustly.

 7. Let me hide/fade out join/leave notifications and other admin messages.

 8. Keep my place so I know what messages are new.

 9. Make it obvious which channel I'm looking at, and even more
 obvious which channel I'm about to type in. (Nothing is great at this)

 10. Spell-check is nice, but autocorrect is awful for IRC and
 technical discussions. Needs a global switch.

 11. Don't show unread counts. Some channels are chatty and I'm just in them listening for my name.

Here are the clients I've tried and why they aren't quite perfect:

## [Colloquy](http://colloquy.info)

Colloquy is a nice full-featured open source client. I've used it the
most. However - it doesn't show multiple channels in one window at the
same time, and doesn't keep your place. I've had some problems with
reconnection, where I thought IRC was quiet when I was actually just
disconnected and didn't know it.

I have to turn autocorrect off for each room I'm in, which I only
remember after the first time it really annoys me by mangling some
jargon.

There's also some general buggy behavior, and I have a short list of
bugs I'd like to report someday, but I don't have time to fix them.

Years ago I hacked my own version of a place marker that I liked, but
I can't remember why it didn't make it in, and of course the code is
lost now.

The backlog search looks like it should be powerful, but in my
experience it just doesn't work - it never displays any results. I'm
not sure what the deal is there.

(As a side note, Colloquy's iPhone app is the only iPhone IRC client
I've used. It seems to work fine, and I don't use it enough to have
specific gripes. Just having to have IRC open on my phone is
guaranteed to annoy me more than the software itself could.)


## [Emacs ERC](http://www.emacswiki.org/ERC)

My current setup is just to run ERC in an emacs window alongside my
code editing.  This has super flexible window splitting and size
management and unbeatable search for your backlog, since it's just
another emacs buffer. There's another nice benefit - if you're writing
about code, emacs' tab-completion for strings across all buffers means
that you can easily autocomplete SomeReallyLongFunctionName in
chats. This saves a lot of typing and cut n' pasting. When you do need
to cut n' paste, it's nicer to do it between emacs buffers than
between apps.

The defaults are not ideal, as usual with emacs you need to dig around
to find a good setup.

There's a module to colorize nicknames according to a hash of the
name, so it's easier to tell people apart. Other clients have similar
features but I think I like emacs' the best for some reason - maybe
the palette is nicer.

There's a module to mark your place that only works if you left the
cursor in the backlog, which is a little weird. It will highlight my
nick when mentioned, but not the whole line.

Since it's open source, I have the same problem as Colloquy, it's
hackable, but I don't really have time for that. And emacs is fun to
hack on, so it's a potentially dangerous time sink.


## [Linkinus](http://conceitedsoftware.com/products/linkinus)

This is a nice client with some minor flaws and a little flakiness. I
liked it but moved on because of minor annoyances.

It has a kind-of nifty "conversation tracking" feature that tries to
highlight messages in a back-and-forth when you hover over it with the
mouse (but only in the currently selected channel). It's not really
that useful, but I think it could be if pushed further. I'd like to
see more clients try this kind of thing, since separating multiple
concurrent conversations is hard on IRC, and it can be hard to avoid
them.

Lets you display multiple channels in one window, but that needs some
improvement. There's just one text-entry field so it's easy to type
something to the wrong channel. 

The split display has some issues. The split channel views don't show
you the channel name anywhere, and in some cases don't even show you
the channel topic, which may or may not be helpful anyway. So it can
take some effort to figure out what channel you're looking at,
especially if there are many of the same people talking on two
channels.

It can save a set of channels as a group, but it doesn't save the
relative sizes of the splits in the group, so if you want to flip
between groups, you'd better be OK with even splits.

Finally, it only supports vertical splits, so with more than two
channels, you just get a couple unreadably long lines per channel.

It has a very barebones backlog search, but it does work.

They've also clearly tried to re-design the account setup / prefs
experience, but I'm not a big fan of an inspector palette - I wanted
to compare settings between two servers and it will only show me one
at a time. This was also the biggest point of flakiness, where some
edits wouldn't commit and I couldn't tell if the settings were being
changed.

## [Textual](http://www.codeux.com/textual/)

Textual is an open-source app
[(github.com/Codeux/Textual)](http://github.com/Codeux/Textual) that
is for sale on the Mac app store. This is an interesting approach that
I think has some merit - people may still contribute code or bug
fixes, but it's also nice to know that if the app ever gets abandoned,
it could be resurrected. That said, I tried building from source to
enable a quick hack once but the master branch didn't build for me, so
they're not trying to make it easy.

It lets me hide some admin messages, has automatic &
manual scrollback markers to keep track of what I've missed.

This has a setting to "Track conversations using nickname
highlighting" but I couldn't really tell what it was doing.

This also has a pretty barebones search, but again, it works.

I tried this for a few days and liked it, but ultimately switched
away, I think mostly because you can't display multiple channels -
there's just one window and it doesn't split up.

## [Mango](http://mediaware.sk/ware/?page_id=35)

I haven't tried Mango. The screenshots in the App Store and feature
listings don't lead me to believe that it's anything significantly
different from the others. I'd be glad to hear from fans, though.


So, what do you use? Have I missed anything great?