<!--
.. title: PyObjC notes
.. date: 2008/02/01 11:07
.. slug: pyobjc-notes
.. link:
.. description:
.. tags: computers, mac, programming
-->


I've been hacking around with [PyObjC](http://pyobjc.sf.net), the Python-ObjC/Cocoa bridge recently, and it's quickly becoming my favorite way to write Cocoa apps. It's really natural to mix Python idioms with Cocoa objects.

The latest version of PyObjC is 2.0, it's installed by default on OS X 10.5, and XCode now includes templates for starting a PyObjC project. There's even code autocomplete in XCode for PyObjC and IB integration, so aside from some smart-indenting issues, writing PyObjC in XCode is almost as natural as writing in ObjC.

I thought I'd post a few nice shortcuts and tips here.

  

You can use tuples for NSRect/Range/Point, for instance, this -

    r = NSInsetRect(((0, 0) ,
                     (100, 100)),
                    10, 10)


creates this NSRect -

    NSRect origin=
           size=>

  

Passing python arrays as NSArray instances (and dictionaries as NSDictionaries) works great, but sometimes you need to pass a C array. The Python 'array' module handles that nicely:

    import array
    g = NSGradient.alloc().
       initWithColors_locations_colorSpace_(
        [NSColor.whiteColor(),
         NSColor.blackColor()],   

        array.array('f', [0.0, 1.0]),
        NSColorSpace.deviceRGBColorSpace())


  

ObjC selectors are just python strings in PyObjC.

    defNC.addObserver_selector_name_object_(self,
      'windowDidResize:',
      NSWindowDidResizeNotification,
      self)
    # or
    self.performSelectorOnMainThread_withObject_waitUntilDone_('doIt:', None, False)
    # or
    if o.respondsToSelector_("fun:"): return o.fun_(a)

  

Finally, something that comes in handy when working with KVC, the  '_' method now defined on NSObjects in PyObjC:

    o = 
    print o._.myKey
    o._.myKey = 44
    # is equivalent to:
    print o.valueForKey_('myKey')
    o.setValue_forKey_(44, 'myKey')

  

That last example is straight from the [NEWS page](http://pyobjc.sourceforge.net/NEWS-2.0.html), where lots of other useful info can be found.
