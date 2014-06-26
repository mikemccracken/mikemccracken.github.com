<!--
.. title: Macsbug in GDB
.. date: 2005/12/26 02:56
.. slug: macsbug-in-gdb
.. link:
.. description:
.. tags: computers, mac, programming
-->


I was digging around the gdb source and found that there's a plugin in there that supports macsbug style screens and commands from within gdb. If you have the XCode Tools installed, take a look at the Readme on your own (OS X) system at the file [/usr/libexec/gdb/plugins/MacsBug/Readme.html](file:///usr/libexec/gdb/plugins/MacsBug/Readme.html)

To invoke it, type this at the GDB prompt:

`load-plugin /usr/libexec/gdb/plugins/MacsBug/MacsBug_plugin`

then

`mb`

and you've got the old split screen with the register contents on the left.

I never used macsbug for anything real, but this still held some nostalgic value.
