---
layout: post
title: "Lock OS X with password and keep WIFI on"
date: "2016-06-26 19:07:08 -0400"
categories: osx, wifi
---

## Keyboard shortcut to lock the system with password.

There is a keyboard shortcut to lock the computer in a breeze. But first you
have to make sure you have the option *require password* selected in the OS X
preferences. If you don´t have this activated then your display will only go to
sleep and will not lock the screen with a password.

*1. First, in the OS X preferences, go to:*

* System preferences
* Security & Privacy
* General
* And activate *"Require password"* and from the dropdown menu choose *"Immediately"*.
![OS X Lock screen preferences](/images/lock_screen_post.png "OS X Lock screen preferences")

*2. Then you only have to use these shortcuts to lock the system.*

`control + shift + eject`

or

`control + shift + power button`

In my mid 2012 MacBook I can use both shortcuts.

## Keeping WIFI on after locking the system.

To keep the WIFI signal on after locking the screen you have to follow this simple steps:

1. Open the terminal to find out which is your wifi device like this:

`ifconfig`

and look for your device. In my case is **en1**. I know it because of the IP address.

Then you have to run this command, in one line, in the terminal:

`sudo /System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport en1 prefs DisconnectOnLogout=NO`

And that´s it. Now you can lock your screen without having to worry about disconnecting from the internet and interfering with your downloads.
