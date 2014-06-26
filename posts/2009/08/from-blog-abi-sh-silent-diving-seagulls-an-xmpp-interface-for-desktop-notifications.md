<!--
.. title: Notifications and Distraction in Webapps
.. date: 2009/08/11 09:29
.. slug: from-blog-abi-sh-silent-diving-seagulls-an-xmpp-interface-for-desktop-notifications
.. link:
.. description:
.. tags: desktopvswebapps, focus, growl, notification, xmpp
-->


Found via Hacker News:

[abi | blog  » Introducing Silent Diving Seagulls: An XMPP Interface for Desktop Notifications](http://blog.abi.sh/2009/silent-diving-seagulls/)

The idea here is that you can use XMPP to let web apps pop up Growl (or libnotify or Snarl, etc) notifications on your desktop. This is a pretty cool hack, and it seems like the right solution to getting notifications from the cloud onto your desktop - as Abi mentions in the post, you don't want direct connections to Growl and you also don't want every site writing its own notify app. It's also another step in blurring the lines between web apps and desktop apps.

However, I think the majority of uses for this kind of notification are distracting and unproductive. The example Abi uses is getting updates from friendfeed - you'd get a notification every time one of your friends does anything on friendfeed. If you think hearing a beep every time you get new mail is distracting, just wait.

About the only use I've found for notifications is to let you know you can get back to work when something long you've been waiting for finishes. I wrote more about this in ['go juggle': an attention callback](http://michael-mccracken.net/wp/2008/08/28/go-juggle-an-attention-callback/).

So notification technology is useful, and it's cool to see web apps getting into it, but please, web or desktop – ship with notifications off. Let's not have the default behavior of your app be distraction.

**edit**: In the [HN thread on Silent Diving Seagulls](http://news.ycombinator.com/item?id=755507), abi notes that he's sensitive to the distraction this can cause, and makes some good points about why it's still a good idea. The best point - if everyone adopts something like this, email goes back to being email and not an overloaded notification scheme.
