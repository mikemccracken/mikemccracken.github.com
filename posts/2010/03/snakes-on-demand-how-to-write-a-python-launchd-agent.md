<!--
.. title: Snakes on Demand: How to write a Python Launchd Agent  
.. date: 2010/03/14 21:23
.. slug: snakes-on-demand-how-to-write-a-python-launchd-agent
.. link:
.. description:
.. tags: launchd, mac, macdev, multiprocessing, programming, python
-->


Suppose you want to write a Launchd agent in Python that communicates using UNIX domain sockets. There's no sample code for that, but the information is out there to figure out how (especially because the [launchd source code][ld] is available). Most search results will tell you that you need to read the [Daemons and Agents Tech Report TN2083](http://developer.apple.com/mac/library/technotes/tn2005/tn2083.html), but it's pretty long and not a great tutorial. A better intro reference is Chris Hanson's blog post ["Launchd: better than sliced bread!"](http://chanson.livejournal.com/179229.html), but that doesn't tell you everything, and doesn't mention Python.

I decided I'd share what I've learned recently to make getting started a little easier. I'll give a short description here and post the resulting code to bitbucket at [py-launchd][bb].

*Note:* This was written and tested on OS X 10.5.8 with the default `/usr/bin/python`, version 2.5.1. 
Since I wanted to use multiprocessing, I used the backport to 2.5 available at [google code: python-multiprocessing](http://code.google.com/p/python-multiprocessing/) . For convenience, it's included in the repository, and so is its license.

### Goal

What we're trying to do is have some python code that gets called when launchd notices someone connecting to a [UNIX domain socket](http://en.wikipedia.org/wiki/Unix_domain_socket). UNIX domain sockets are local-only, so this is ideal for agents that only serve local apps. We're also using launchd "agents" not "daemons", so we're assuming that it's OK to have one agent process for each user. If you're managing access to something that needs to be unique system-wide, then this won't work (but you can still use Launchd).

### launchd overview

The launchd process will read a launchd plist you give it (at login, via launchctl or the 10.6 framework), and listen on the socket you tell it to. Once it sees a connection, it'll start the agent program you specified in the plist, and that program can make some calls using the launchd C API to get a file descriptor for the socket that was connected. This is important - you don't need to call bind() or listen() on the socket, because launchd already did. It's just handing the open socket's file descriptor straight to you and your code can just call accept() on it.

### Using launchd with Python 

You need to create a C/ObjC tool that can do the launchd check-in to get the open file descriptor, then pass that off to your Python code. This is pretty straightforward using the Python framework included in OS X and the Python C APIs.

What I've done is create an agent loader that I called PyLaunchd that loads and runs server code in Agent.py. It expects Agent.py to be in the same directory.

PyLaunchd is built separately and copied into the test app's Resources folder with an XCode script phase.

I have the app delegate copy `PyLaunchd` and `Agent.py` to `~/Library/Application Support/PyLaunchd/` on loading.
It also customizes the launchd plist to set the path correctly for the current user, then writes that to `~/Library/LaunchAgents/`, and loads it. (Actually it first unloads it, then reloads it. I'm not convinced this is the right way to do it). It uses system() to call launchctl, but I believe in OS X 10.6 there's an API you can call to do it directly.

Finally, the sample app is really simple - it just opens the socket using the multiprocessing Client class, and sends whatever you type. The example Agent I've included will ROT13 it and send it back.

Please let me know if you have any comments, questions, or improvements.


[ld]:http://launchd.macosforge.net
[bb]:http://bitbucket.org/mikemccracken/py-launchd/
