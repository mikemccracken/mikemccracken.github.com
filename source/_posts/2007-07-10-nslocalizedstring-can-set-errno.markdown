---
comments: true
date: 2007-07-10 10:27:34
layout: post
slug: nslocalizedstring-can-set-errno
title: NSLocalizedString can set errno
wordpress_id: 108
categories:
- mac
- programming
---

This is a short one, but it might help someone with debugging someday.

A while back, we had some code that was checking errno, then using the NSLocalizedString macro to get a localized error message, but it checked errno again later. Only the app isn't localized yet. There's no Localizable.strings file, so when NSBundle -localizedStringForKey gets called, even though it fails gracefully, it still ends up setting errno to "ENOENT", or "file not found".

So the lesson is - in case you're seeing weird behavior where errno is changing after you check it, make sure you're not using any system calls that might set it.
