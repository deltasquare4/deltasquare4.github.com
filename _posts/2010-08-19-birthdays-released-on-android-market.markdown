---
author: deltasquare4
date: '2010-08-19 18:31:25'
layout: post
slug: birthdays-released-on-android-market
status: publish
title: Birthdays Released on Android Market
wordpress_id: '163'
categories:
- Android
- Learning Log
- News
tags:
- Android
- Application
- Birthdays
- Market
- open source
- Reminder
---

Yesterday, I released my first Android application on Android Market - Birthdays. It is a birthday reminder application which syncs all your contacts' birthdays to your calendar.

One can say that I'm a forgetful person and while there are some advantages of this situation, I often forget birthdays of people who matter. As a solution to this, I started maintaining birthdate of a person into his/her contact. Back then, I had just bought an iPhone and I was pleased that it had a "Birthday" field in the address book. I didn't hesitate paying $0.99 for a [birthday reminder app](http://itunes.apple.com/app/birthdays-anniversaries-more/id292248810?mt=8) which didn't exactly "remind" me (iPhone didn't support Push notifications or Calendar sync back then).To be exact, it helped only a little if at all.

In the same time period, I was also excited about [Android as a development platform](http://www.rakshitmenpara.com/blog/2009/08/12/android-development-for-beginners/). When I got my [first Android device](http://www.rakshitmenpara.com/blog/2010/06/05/expectations-and-initial-impressions-of-htc-desire/), I tried out a few birthday reminder apps already available. Most of them didn't work as I expected them to. While some did, they relied on a background service for notifications which will keep running at all times. So, I decided to start the development of yet another birthday reminder application which will get the job done while not being a resource-hog. While the journey of the development was quite educational, it was easier than I initially thought (probably because of a [slight change in my job description](http://www.rakshitmenpara.com/blog/2010/07/24/episode-ii-return-of-a-freelancer/)). I still can't believe it took me a year to developand publish my first "real" application.

So, what's next? The application is still very basic. I am going to explore android SDK some more by adding new features like facebook sync, two-way contact sync etc. I have had a lot of help from Android developer community so, I am going to write a few blog posts explaining some issues I faced in the development of this application as my contribution. <del>I am also planning to open the source to public as soon as I am done with implementing all the features I have in my mind.</del> The application source can be accessed from [Github](http://github.com/deltasquare4/Birthdays).

**Note: Because of a major bug, all the calendar events created by Birthdays are being removed by Android upon reboot. I have pulled back the application from market because I couldn't find a stable solution.**

