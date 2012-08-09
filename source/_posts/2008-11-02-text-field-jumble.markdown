---
comments: true
date: 2008-11-02 14:38:46
layout: post
slug: text-field-jumble
title: iCal's Text Field Jumble
wordpress_id: 121
categories:
- mac
- programming
tags:
- cocoa
- mac
- programming
- ui
---

I've written here before about text fields, particularly the problem of having a good-looking 'display' mode and a separate 'edit' mode for data you don't edit so often, like in AddressBook.

The most recent version of iCal decided that events are write-once-read-many as well. You now have to use cmd-E to get into edit mode, while cmd-I just gives you a small display mode.

I'm mostly OK with that, although I find I edit events about as often as I look at their info windows - after editing I usually just deal with alarms, not the events themselves. The casual glance at the time and title is always enough - I think either you're looking at the time and title or you're editing. I don't see the appeal in the new 'info-only' mode (if it's actually new - it seems new.)

However, the change does highlight the jumble of editable text fields and text-like fields in the edit window:
[![](http://michael-mccracken.net/wp2/wp-content/uploads/2008/11/pastedgraphic-1.tiff)](http://michael-mccracken.net/wp2/wp-content/uploads/2008/11/pastedgraphic-1.tiff)

[![](http://michael-mccracken.net/wp2/wp-content/uploads/2008/11/pastedgraphic.tiff)](http://michael-mccracken.net/wp2/wp-content/uploads/2008/11/pastedgraphic.tiff)

The "Add Attendees" link and the "None" placeholder for url act the same - you click on them, and enter text.
One's a link and one's mute gray text. Why?
For my part, I think the gray text is too understated, and the link is too garish.

There are other differences: you can tab to the "url" field, but you can't tab to "attendees"... until you add one, then you can. Once you click on either of them, the url field pops up a plain white raised NSTextField, but the attendees field is sunken and translucent, apparently an NSTokenField?

Both of the blue links could also be buttons. I'm still not completely sold on replacing buttons with links, but I can understand the trend. I think a small plus-sign button would be fine for "Add File", though, and "Attendees" ought to be a text field. Why force the user to use the mouse when adding data to an event?

All in all, I think the "Add Attendees" link/field is pretty strange. I'm curious if I missing a precedent somewhere.
