---
date: '2010-08-31 21:33:32'
author: deltasquare4
layout: post
slug: working-with-stateful-listview
status: publish
title: Working With Stateful ListView
wordpress_id: '175'
categories:
- Android
- Learning Log
tags:
- Android
- Birthdays
- Development
- ListView
- Programming
- Stateful
---

**What is Stateful ListView?**  
It's not a coined term, but it's obvious. Stateful [ListView](http://developer.android.com/reference/android/widget/ListView.html) is a listview whose items change according to its state.the state is usually maintained by a custom [ListAdapter](http://developer.android.com/reference/android/widget/ListAdapter.html).

**Why would I need it?**  
I don't know. But, I can tell you why did I need it. In my [Birthdays](http://www.rakshitmenpara.com/blog/2010/08/19/birthdays-released-on-android-market/) application, I wanted to have a "Batch Edit" mode. When activated, it should allow users to mark multiple items using checkboxes. That means these checkboxes weren't part of my "Standard" mode. I didn't want to create whole new activity just to add a checkbox. So, I decided to have the checkbox in the hidden state by default. I wanted to somehow loop through all
the items and make it visible.

**Sounds pretty easy. What's the problem?**  
The first one isn't actually a problem. It is because of the way Android is designed. The ListView doesn't load all the item at once to optimize memory management. Only visible items are loaded. So, one can't exactly loop through all the items because they don't exist. If you change only visible items, newly rendered items after scrolling don't have the change. The new items are rendered by executing `ListAdapter.getView()` for each item. So, maintaining the state inside the adapter solves the issue.

Now all the new items are being rendered correctly but, it won't change the already rendered (visible) items. To solve this, I combined the above two techniques - maintaining the state inside the ListAdapter for items not yet rendered and looping through all the visible items and changing them. This introduces another issue that consumed more time in identification and resolution then before.

Basically, if user switches between modes when the ListView is being scrolled, Android VM will throw NullPointerException because the requested ListItem doesn't exist in the view.

**What did you do?**  
The cause of this was the loop where I was trying to modify the items. When the function was being invoked, because of the still-scrolling ListView, indexes of visible ListItems changed and they were no longer available. I had to remove it for starters. Now, what I needed was a strategy to make the checkboxes visible for already rendered items. After a little bit of searching I found out that by calling `Adapter.notifyDataSetChanged()` I can re-render visible ListItem views. If anybody has an improved strategy to implement the scenario, please comment below. I will update the post accordingly.

The source code for Birthdays application I mentioned above can be accessed via [Github](http://github.com/deltasquare4/Birthdays).
