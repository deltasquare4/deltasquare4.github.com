---
author: deltasquare4
date: '2009-07-28 11:09:42'
layout: post
slug: cydia-crashing-on-startup
status: publish
title: Cydia crashing on startup
wordpress_id: '17'
categories:
- Articles
- iPhone
- Learning Log
---

I was just updating some applications through cydia the other day and my wifi connection went down while update was in progress (damn power outs... yeah, we still have a lot of them in India).

Now, after the incident, whenever I tried to open Cydia, it crashed while loading database. I tried rebooting the device a couple of times with no luck.
Still Cydia kept crashing. I googled a bit about cydia startup crashes. Most of them were from much older OS (v1.1 really seems much older compared to v3.0
installed on my iPhone) and remaining solutions didn't work for me.

Now, having your jailbroken iPhone with Cydia not working is pretty bad. So, I kept searching and I found out that Cydia writes a log file at /tmp/cydia.log. I opened that file using mobile terminal (also can be done via SSH) and there it was. One package was corrupted (Error message being "Unable to parse package file /var/lib/apt/lists/). I just removed the corrupted package file from specified location and voila. Cydia is now working as it was previously :)

Hope it helps...

