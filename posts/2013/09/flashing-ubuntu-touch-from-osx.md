<!--
.. title: Flashing a Nexus device with Ubuntu Touch from Mac OS X
.. date: 2013/09/12 10:40
.. slug: flashing-ubuntu-touch-from-osx
.. link:
.. description:
.. tags: ubuntu, nexus, ubuntutouch
-->


I've been working with Ubuntu Touch recently, using VirtualBox to run
Ubuntu Saucy as a guest on my Mac, and while it does work to connect
to the device once it's installed, the process of reflashing is
difficult. The manual steps on the Ubuntu Wiki
[Touch/Install](https://wiki.ubuntu.com/Touch/Install) page work for
the old way, via `phablet-flash cdimage-touch`, with the caveat that
you may have to manually reboot the device and/or re-connect the USB
in between steps.

However, as of [this email last week][sysimage-msg], the official way
to flash phones is using the system images via `phablet-flash
ubuntu-system`, which has a different set of files.

Instead of just muddling through and updating the manual instructions,
I decided to see if phablet-flash would run natively on the Mac. After
a bit of python dependency resolution, it does. Here's what I did:

1. Download the [Android SDK tools][androidsdk]. You only really need the "SDK Tools", not the whole ADT Bundle, so I clicked on "Use an existing IDE" at the bottom of that page, to get the smaller installer.
2. Unpack the archive and run ./android. Install the platform-tools (and nothing else).
3. Add the platform-tools/ directory to your $PATH for convenience.

4. (Optional) create a virtualenv for the python dependencies, and activate it.
5. `pip install` each of `configobj` `pyxdg`, and `pyliblzma`
6. get [bazaar][bzr] if you don't already have it.
7. branch phablet-tools: `bzr branch lp:phablet-tools`
8. `cd phablet-tools && python setup.py build`
9. At this point, `phablet-flash ubuntu-system` should work smoothly, with all transfers and reboots and timeouts going as expected.

The only minor hiccup is that it apparently doesn't get ~/Downloads/
from pyxdg, but it just means that you'll get the images saved to
~/phablet-flash instead of ~/Downloads/phablet-flash. No big deal.

[sysimage-msg]:https://lists.launchpad.net/ubuntu-phone/msg04004.html
[androidsdk]:http://developer.android.com/sdk/index.html
[bzr]:http://bazaar.canonical.com/