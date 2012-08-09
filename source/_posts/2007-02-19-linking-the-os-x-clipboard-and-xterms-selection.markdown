---
comments: true
date: 2007-02-19 18:23:22
layout: post
slug: linking-the-os-x-clipboard-and-xterms-selection
title: Linking the OS X Clipboard and XTerm's selection
wordpress_id: 90
categories:
- mac
- tips
- X Windows
---

If you only use X11 for XTerm, it might seem like the handling of the clipboard in Apple's X11.app is broken. You can select text and paste it with a click of the middle mouse button (opt-click on my Powerbook), and that works when pasting into other X apps, but it doesn't change the Mac clipboard at all.

Why not? Is X11.app just ignoring the X clipboard?

No - X11.app *does* synchronize the two clipboards. The problem is that the selection pasting in XTerm is using a completely different buffer. There's a full and clear explanation, with some interesting details about (X)Emacs' behavior, at [jwz.org](http://www.jwz.org/doc/x-cut-and-paste.html).

If, like me, you only use X11 for Emacs and XTerm, you might want to link the selection in XTerm to the X clipboard, so X11.app will then sync that with the system clipboard and you can select in XTerm and paste with Cmd-V in say, Mail.app.

I'll tell you how in a sec, but first the caveat - I said if you only use X11 for Emacs and XTerm because what we're going to do is make setting the XTerm selection always overwrite the clipboard contents. If you use X apps that use the X clipboard, sometimes you don't want that. So beware. If you use Emacs, it just pushes onto the kill ring, so you're good.

OK, now that that's over, add these lines to your ~/.Xdefaults:


    
    
    XTerm*VT100.Translations: #override\
    <BtnUp>: select-end(CLIPBOARD,PRIMARY)\n\
    <Btn2Down>: insert-selection(PRIMARY)\n\
    



Note that the backslashes at the end of the lines are important.

Update: The first version of this post didn't include the Btn2Down action. Without that, the original paste behavior goes away - the man page doesn't really explain the "#override" keyword, so I'm not sure why.
