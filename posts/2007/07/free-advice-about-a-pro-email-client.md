<!--
.. title: Free advice about a pro email client
.. date: 2007/07/06 09:54
.. slug: free-advice-about-a-pro-email-client
.. link:
.. description:
.. tags: email, mac
-->


If you're thinking of writing a commercially successful *pro* email client for Mac OS X, here's some advice along the lines of what I wrote [yesterday](http://michael-mccracken.net/wp/2007/07/05/it-could-work-a-3rd-party-email-client-for-os-x/):

*Make sure you've tried a lot of email clients.* Try everything you can get your hands on. Really use each one - figure out what makes it different, and what makes it powerful. Make sure you've tried text-only clients like mutt and pine. Lots of your target audience refuses to give those up - figure out why. Don't just try free alternatives - peek in on big-business. Fire up Parallels and try Outlook and Notes in Windows (there may be others that are even better examples). Read up on the [Chandler project](http://chandlerproject.org/Projects/WebHome).

*Make sure the email is always available in an open data format.* If this isn't obvious, you should probably stay home. Keep a backup copy of email in something Apple Mail can read - like Unix mbox files. You can use a database for tags and whatever, but there had better be mbox files around, because your target audience won't move into an app they can't move out of.

*Don't start out by cloning Apple Mail.* If your first screenshot looks almost like Mail but does less or isn't as pretty, it's bad news. Mail is a big program with lots of time and effort behind it. If you try to match its feature list first before you make your client unique, you're toast.

*Pick a specific customer, and get to know their email problem.* Why not clone Apple Mail? Because you're not writing for the same customer, are you? Make sure you know who your customer is, and what they actually *need*. People who want a pro app probably already have a system for to-do lists & notes, so your client doesn't need to match those features. Likewise, email pros can still use Mail to send slideshows to Mom…

As an example, since you're probably a programmer, think about how a programmer's email client would be different from the standard. Maybe it does syntax highlighting. Maybe you can apply patches people send you with one click. Maybe you can create bugzilla issues from an email with one click. Or collaborate on a support email with the [SubEthaEngine](http://www.codingmonkeys.de/subethaengine/). Nobody but programmers will want to use that client, but that's fine - there are lots of programmers. Now what about music and video editors? Graphic designers? See where I'm going?
