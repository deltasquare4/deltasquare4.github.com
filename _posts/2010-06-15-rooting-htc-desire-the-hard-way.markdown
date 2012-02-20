---
author: deltasquare4
date: '2010-06-15 22:05:04'
layout: post
slug: rooting-htc-desire-the-hard-way
status: publish
title: 'Rooting HTC Desire: The Hard Way'
wordpress_id: '96'
categories:
- Android
- Learning Log
tags:
- Android
- HTC Desire
- HTC Desire Rooting
- Rooting
---

There are many HTC Desire Rooting tutorials and step-by-step guides out there. Best ones amongst them are probably [this](http://forum.xda-developers.com/showthread.php?t=696189) and [this](http://android.modaco.com/content/htc-desire-desire-modaco-com/307365/14-jun-r6-riskfreeroot-htc-desire-rooting-guide-now-with-hboot-0-80-and-os-to-1-21-support/). There are easier methods like [this](http://android.modaco.com/content/htc-desire-desire-modaco-com/308542/r4-htc-desire-easy-rooting-guide-with-tiny-core-linux/), but I prefer simpler over easier (Yup, I'm too lazy to burn a CD. I'd rather do it without rebooting :P). Before proceeding with the process I followed, I should mention that my HTC Desire is Singapore/Unlocked version which comes with [RUU_Bravo_hTC_Asia_WWE_1.19.707.7_Radio_32.36.00.28U_4.06.00.02_2_release_126179_signed.exe](http://shipped-roms.com/shipped/Bravo/RUU_Bravo_hTC_Asia_WWE_1.19.707.7_Radio_32.36.00.28U_4.06.00.02_2_release_126179_signed.exe) ROM by default.

I primarily used Snow Leopard for this process (I had to use windows to make GoldCard). Following the above mentioned xda-developers guide pretty much did it. As it mentions, even I don't have a branded (career locked) ROM, I needed a GoldCard to make it work (I came to know that after couple of failed attempts :P). Anyway, following the guide for Mac OS X, everything else worked perfectly till the time came to restart device in recovery mode and flash update.zip from SD card. It failed to flash it because image verification failed. So, after spending some time on internet trying to find a solution, I finally found one. I found a way to enter a custom flasher menu in recovery mode by executing recovery-mac.sh (Which loads the green menu mentioned [here](http://forum.xda-developers.com/showpost.php?p=6710081&postcount=2)). It took me a while to figure out that this menu doesn't operate with volume up/down like the bootloader. So, here is the tip - **The green recovery menu can be navigated using optical trackball; so it's not stuck or frozen **:P

So, finally I have my HTC Desire rooted. First thing I did was to get rid of the stock ROM. I took the Red Pill ([Pays-ROM 2.0](http://forum.xda-developers.com/showthread.php?t=674688)) and installed the ROM. Let's see if I can find any difference in speed and battery usage.

**Update: **My desire keeps restarting if I click on new text message notification (More on that here). So, reverting back to the stock ROM for now. I hope I can work on my own ROM soon enough before I lose interest or I find a perfect ROM :)

