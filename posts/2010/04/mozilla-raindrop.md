<!--
.. title: Mozilla Raindrop
.. date: 2010/04/15 11:12
.. slug: mozilla-raindrop
.. link:
.. description:
.. tags: bulk-mail, mozilla, mozilla-labs, raindrop, wave, webmail
-->


A little while ago I noticed the [Mozilla Raindrop](http://labs.mozilla.com/raindrop/) project. It's an interesting project in Mozilla Labs by the Thunderbird team.

It's trying to rethink how messaging (in general, not just email) should work - using open web technologies. On the surface it sounds like Google Wave, but I'd say it's aiming a little lower - trying to take existing protocols and build software that handles them all together in a better way. I also think it's a better approach than Wave, focusing on designing a single artifact that people will want to use instead of a framework technology demo, which is what Wave always seemed to me.

It looks like it's not intended to be a native desktop (or mobile) client - they mention running it on servers, and it depends on Python and CouchDB, which would preclude it running on the iPhone OS.

One of the things I like about it is the way they're trying to use a classification of emails - obviously, not all mails are equal. They fall somewhere in a range between spam and important personal (or work) messages. A big class is "bulk" mail - mail that's useful but not necessarily of a conversation involving you. Mailing lists, promotional mails you've asked for, facebook/twitter notifications might all fall into this category, and it's a great idea for a mailer to do something different with them. At the least, it should let you ignore them if you're just trying to do a quick processing pass of new mail.

The [Raindrop design blog](http://blogs.mozillamessaging.com/raindropdesign/) has some good posts (with plenty of screenshots) outlining their current approach.