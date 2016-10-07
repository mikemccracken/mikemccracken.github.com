<!-- 
.. title: What to do with Photos 2015
.. slug: photos-2015
.. date: 2014-08-05 09:26:17 UTC-07:00
.. tags: photos, flickr, git, git-annex
.. description: Photo management and archiving is not getting better
.. type: text
-->

It's 2015, and saving and making use of digital photos and videos is too hard, and doesn't seem to be getting better.
I still have printed pictures of my parents when they were younger than me, because they were in an album somewhere.
But I need to get serious with some kind of digital media strategy, or my kids might not be able to find or access any pictures of themselves as babies.

We have a couple Macs, some iPhones and some cameras with SD cards. We
want to back up photos to one place, permanently prune out bad ones,
and be able to access all of them in an organized way that lets us
e.g. upload them to places to get yearly books printed.
This basically means we need the stuff in the cloud, with an easy way
to download subsets onto local disks.

So, we need some kind of server-hosted solution, and there are so many
it's hard to keep track.  I looked into most of them, and read a few
summary posts, and so many of them don't quite make it easy to import
from everywhere, or they leave me uneasy that I'll have to switch
again sometime soon. Big companies abandon their products, and small
companies get acquired then abandon their products often enough that
almost any for-pay service feels temporary. Free services, or platform-tied things like iCloud, Google plus or Amazon Prime Photos also feel temporary, because they're tied to the success of that platform (and what if I decide to change phones?)

Last summer, I spent a lot of time working with git-annex because I
liked the flexibility of not having to keep all the photos in one
place but still have them in one logical 'annex' with their location
being tracked - and I wanted to control the backup of the data.  I
even spent a long time on an import script that avoided dupes and
tagged photos with git-annex metadata from their GPS info.  The neat
database-like "view" features built around metadata turned out to be
unusably slow with >1K files, though, and so I was looking at more
work trying to help fix that, along with still needing to figure out
what to do with the iPhones, and it just seemed like too much effort.

So, I looked back at reviews of hosted sites (I thought it was from sweethome.com, but I can't find it there anymore),
and saw that [Picturelife](http://www.picturelife.com) 
allows you to use your own bucket on Amazon S3 for photo storage -
then you get the Picturelife features for free and only pay Amazon for
storage. So if Picturelife dies for some reason, your bucket still has
your photos. I thought that sounded pretty good, so I've been trying
it out for a while. I like their import features - there's a mac app
that I used for the initial bulk upload and ongoing for emptying the
SD cards, and the iPhone apps work as well as apps can be expected to
(background uploading seems to not work or not be implemented).

I have some UI nits to pick, but overall it is good - lets me look
through pictures (I haven't bothered with the editing UI yet), and
hide or delete bad ones, tag and write captions. All good so
far. There's a map view that's interesting but has equally interesting
bugs - I reported one where photos from Portland, OR were sometimes
interpreted as being in Portland, Maine for example. And it'd be nice
to be able to say "show me this picture on the map", but that
direction isn't implemented.

Since I wrote the last paragraph, none of my bugs have been fixed, and Picturelife's incredible journey
[has been acquired](http://blog.picturelife.com/post/109541575280/picturelife-joins-streamnation). I'm
currently just waiting to see how that changes things - they say it'll continue as a product.
At least my photos are in my own bucket.

If only there was an easy obvious choice. What do you do?