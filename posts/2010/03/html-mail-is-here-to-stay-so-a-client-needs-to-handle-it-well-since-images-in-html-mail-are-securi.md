<!--
.. title: HTML mail is here to stay, so a client needs to handle it well. Since images in HTML mail are securi
.. date: 2010/03/31 12:00
.. slug: html-mail-is-here-to-stay-so-a-client-needs-to-handle-it-well-since-images-in-html-mail-are-securi
.. link:
.. description:
.. tags: addressbook, gmail, html, image, thunderbird-3, whitelist
-->


HTML mail is here to stay, so a client needs to handle it well. Since images in HTML mail are security problems, a good client won't load them until you say so - and should also let you white-list some senders.

GMail does this well enough, with two links - one to show the images in a message once, and another to whitelist the sender. I'd say that's about the best you can ask for. If you want to remove a sender from the whitelist, it's a little obscure - you have to find an email from them and there's a link in the details that says "Don't display from now on."

![GMail image whitelist](http://media.tumblr.com/tumblr_kzulamJin51qz505e.png)

One interesting thing is that this is a separate list of addresses from your Contacts (which in GMail, includes every address in every email by default).

Thunderbird starts off with basically the same interface as GMail. They show a big loud bar that alerts you to the missing images, as if you couldn't tell. You can press a button to load it once, or click a link (why not another button?) to whitelist the sender.

![Tbird image whitelist](http://media.tumblr.com/tumblr_kzulcqQ6PG1qz505e.png)

This is where we go a little haywire, though - all I want to do is whitelist the sender for images, but Thunderbird throws up a sheet asking me for all kinds of contact info - now the sending email is in my address book. So I end up with a bunch of noreply addresses in a group in my address book called "Personal Address Book." Thanks?

![Tbird addrbook](http://media.tumblr.com/tumblr_kzull57mRg1qz505e.tiff)

I think a whitelist just for image display that's separate from the address book is the way to go - it seems more natural. An address book seems like something I should control manually. Ideally, in a desktop mail client on OS X, the client's address book is just the system's Address Book DB - so that other apps can use the info. And since that's system-wide data, you really don't want a client just dumping everything in there.
