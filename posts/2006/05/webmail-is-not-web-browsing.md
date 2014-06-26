<!--
.. title: Webmail is not web browsing.
.. date: 2006/05/11 05:00
.. slug: webmail-is-not-web-browsing
.. link:
.. description:
.. tags: computers, mac, programming, web
-->


Webmail is really a separate application. When I'm visiting GMail, I'm *checking mail*, not browsing the web. So what's so bad about using a browser for this?

### Minor Gripes

If I keep a browser window running with GMail, now clicking on the Safari dock icon just brings that sucker up instead of creating a new empty window.

I love the GMail key shortcuts and Safari has an annoying tendency to get the key focus wrong so I have to click in the window somewhere after moving up out of a thread to get my shortcuts back.

Safari crashes, I forget to reload GMail, I miss important messages.

Even all that isn't so bad. For a while I ran Firefox with only GMail open. I could get a GMail notifier so I won't miss messages... but:

### The *Real* Problem

The final straw is this: Every time I check mail, I'm diving right into the world's biggest time-sink. My email isn't usually a waste of my time, but all the windows I've left floating around, my bookmarks bar, or a quick Google search are. These are the things that eat up afternoons, and webmail is a gateway to that distraction.

Browsers have lots of features that I don't need to use GMail: bookmarks, back & forward buttons, a search field, page history, a location bar, and on and on.

### My Easy Way Out - the Minimalist Specialized Browser

A while back, I wrote a separate web browser just for GMail.

All it does is load GMail in a nice big window and duck out of your way. *No location bar*. And *no bookmarks*.

It says: Go ahead and follow that link your friend (or bug tracker) sent you, but to check BoingBoing, you're going to have to go over to Safari. Maybe you'll decide to go back to work instead.

It's basically the WebKit demo, except that I tried to improve the key shortcut situation a bit, and it has a progress indicator.

I've been using it for a while now, and the only features of real browsers that I miss are pretty simple to add - text find, a refresh command. I just haven't needed them that much. <del>Sadly, one feature I'd love to add to GMail, a key shortcut to "go to inbox", eludes me, since their Javascript is pretty obfuscated.</del> Update - "go to inbox" already exists as the sequence "gi".

### Meet WebMail.app

If you want to try out this  idea without the hassle of writing those ten lines yourself, get a tarball here: [Webmail-1.0.tgz](http://michael-mccracken.net/webmail-1.0.tgz) and let me know what you think.

The source is in there, it's BSD licensed, and I'll happily accept patches that make it more useful for email, but remember that making it more useful for general browsing is kind of not the point.

Oh, and it lacks a real icon. Sorry.

*Update* much later: a new version that supports printing and attaching files is available here: [Webmail+printing+attaching.zip](http://michael-mccracken.net/2007/WebMail+printing+attaching.zip)
