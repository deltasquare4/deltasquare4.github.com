---
author: deltasquare4
date: '2010-08-07 09:29:07'
layout: post
slug: installing-redmine-1-0-on-mac-os-x-snow-leopard
status: publish
title: Installing Redmine 1.0 on Mac OS X Snow Leopard
wordpress_id: '151'
categories:
- Learning Log
tags:
- Mac OS X
- Project Management
- Rails
- Redmine
- RoR
- Snow Leopard
---

I have been a great fan of [Redmine](http://www.redmine.org) since I came to know about it back in 2008. I have been using it ever since to track my personal as well as professional projects. I had an installation of good old Redmine 0.8.6 on my Snow Leopard and I decided to upgrade it to 1.0 RC. As always, installation was not so smooth for me, but I managed to do it and here's how.

I followed Redmine [Upgrade Instructions](http://www.redmine.org/wiki/redmine/RedmineUpgrade) initially, which required me to upgrade to Rails v2.3.5 from v2.2.2 with all dependencies. Thanks to awesome rubygems, it was a cakewalk. But, I made a rookie mistake there. Instead of installing them in system path using `sudo`, I installed them in user directory (`~/.gem`). To check your gem installation location, you can execute `gem list -d`. Anyway, it eventually led to an error _"Missing the Rails gem. Please `gem install -v=2.3.5 rails`, update your RAILS_GEM_VERSION setting in config/environment.rb for the Rails version you do have installed, or comment out RAILS_GEM_VERSION to use the latest version installed"_ . This was very confusing as Rails 2.3.5 was already installed and upon executing `rails -v`, it displayed Rails 2.3.5. I had to uninstall Rails 2.3.5 and all the dependencies from user directory and reinstall them in system path using `sudo`.

Second challenge was to make Rails 2.3.5 work with mysql. As I was using default mysql installation in snow leopard, which happens to be a 32-bit one, I was not able to install mysql gem for ruby. After a little bit of googling, I found out that I had to download and install 64-bit MySQL in order to compile 64-bit gem. So, I installed new MySQL instance, migrated all my data from the older instance and then installed mysql gem. And I finally got the new Redmine installation got up and running on apache.

I wish I can have the wordpress-like automated upgrade mechanism in Redmine.
