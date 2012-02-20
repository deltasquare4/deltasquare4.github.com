---
author: deltasquare4
date: '2010-02-20 23:50:56'
layout: post
slug: my-bios-speaker-wont-stop-beeping
status: publish
title: The Continuous BIOS Beep Crisis
wordpress_id: '76'
categories:
- Learning Log
tags:
- BIOS
- Continuous beep
- EP45C-DS3R
- Gigabyte
- non-stop beep
---

I have faced a weird BIOS issue today. Apparently, I was cleaning up the dust on my CPU heatsink. When I booted my machine after I was finished, first it started with single beep immediately followed by a never-ending beep. My machine started without any glitch but the beep sound won't stop. BTW, I am running a Intel C2D E8400 on Gigabyte EP45C-DS3R.

So, I immediately checked my CPU and system temperatures. They were normal. Even tried finding similar issue (and a solution) on the web with no luck. As my system was working perfectly, I decided to go ahead and remove the detachable BIOS speaker. But, the problem here was not solved; I've just found a way around it. I couldn't resist myself and dug deeper to find an explanation of this unusual (and undocumented) behavior. After spending some time, I noticed that my CPU fan was running but, in BIOS Monitor, the CPU Fan speed was zero.

Looks like it is a built-in warning to notify that CPU Fan is not running. Disabling the CPU Fan Monitoring in BIOS did the trick. That left me wondering how did I fry my CPU Fan Censor when cleaning it? Anyway, glad that all is well again. :)

Note: This machine is still running as of January 2012 (and will keep doing so for a couple more years). With 8GB RAM and 3+TB disk space, it's my testing/file server now.
