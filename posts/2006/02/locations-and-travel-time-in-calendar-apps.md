<!--
.. title: Locations and Travel Time in Calendar apps
.. date: 2006/02/24 17:05
.. slug: locations-and-travel-time-in-calendar-apps
.. link:
.. description:
.. tags: mac, ical, mac, ui
-->


Now that we've got Google Maps, I'd like to see my calendar program (iCal) extended to pay more attention to the location of events. Show me how long it'll take to get to events I've scheduled, based on where they are. Traffic estimates would make this really killer (at least here in So-Cal)

It might sound like you would need to tell the app where you will be at every point of the day for this to work, but you could avoid that by storing a 'coming from' location for each event - it *could* be the previous event, but you could also just pick it from a list of default places, like 'Home', 'Work', and 'Hockey Rink'.

In my dream world, they'd look like error bars on a plot, they'd even have data about variability of the traffic estimates, and they'd be in the next version of iCal.

Here's a quick visual, in case I didn't describe it well enough:



![](http://michael-mccracken.net/img/traveltime-mockup.png)



Assume home is south of the office and the basketball court is north. Traffic is bad going north around 6. What it's telling you now is you can go home fast, and have 30 minutes there before you have to leave again, go straight to the court, taking 45 minutes in traffic and getting there 45 minutes early, or have about an hour at the office, wait out traffic, and get to the court on time in about 25 minutes.

Update: I changed the example to be a little clearer - I added an option to show traffic choices, showed the times by the routes, and made one event appear selected, since you probably only want this extra info for the selected event.

I also made it a basketball game because everyone knows you'd need to go home to get your gear if you were going to the rink anyway. Seriously.
