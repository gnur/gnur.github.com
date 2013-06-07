---
layout: post
title: "setting up windows 8 for non tech savvy users"
description: "a short guide on setting up Windows 8 for the non-tech-savvy users"
category:
tags: ["windows 8", "how-to"]
---
{% include JB/setup %}

# My thoughts about Windows 8
After installing & configuring Windows 8 on at least 20 pc's & laptops I now have a streamlined approach to setting up a fresh Windows 8 install. This guide will provide short instructions to set up Windows 8 without fighting the new interface and make it behave like earlier Windows versions as much as possible. These instructions assume an English Windows version, the last step will be to change the language of the OS.
A lot of people believe Windows 8 is a terrible operating system. I can't agree. It's fast, looks good, has some great power user tools and seems to boot on just about any hardware made after 2005.
There are some downsides however.

### The good
- booting windows 8 takes seconds, not minutes. This is due to some sneaky semi-hibernating which in itself is a good thing, but does present some issues because a "clean" boot isn't always a real clean boot.
- the new start-screen, with all of it's search options __rocks__.

### The bad
- the default settings make a lot of use of the metro-style applications. Which do not feature the common user interface elements that most Windows users have grown accustomed to.
- the games are gone (big deal for some people)
- the lock screen has no real purpose on desktop machines, it only delays login


## Installing software
I would advise using [ninite](http://www.ninite.com) to install the basic things like browser plug-ins, zipping tools, browsers, antivirus & office. My personal recommendation is to select the following: Chrome, Avira, 7-Zip, Java, Air, Shockwave, LibreOffice, Foxit Reader & TeamViewer (More on that later). The upside of using ninite is that you can save the installer and run it later to update all the packages (if you run it often, you won't even get those annoying pop-ups with updates available).
I believe that maybe 90% of the users won't need more software then these packages.

## Managing the start screen
The start screen should probably be kept as clean as possible, you probably don't need shortcuts to the (metro-styled) calendar & mail app.
The quick way to remove all the unnecessary apps is to right click them all and then select the __Unpin from Start__ option in the bottom of the screen. You should probably leave the Desktop shortcut on the start screen, I would even suggest leaving that one as the only option. That way, the user that logs in will only have the desktop option when logging in and will then be presented with the desktop environment.
If you accidentally remove the desktop shortcut, you can add it again by
- going to the start screen
- search for desktop (just type it, this will start the search through your apps)
- right click the small desktop tile and select __Pin to start__ in the bottom of the screen

## Fix file associations (to prevent metro apps from popping up)
By default, Windows 8 tries to open nearly all media files with a metro application. This is quite annoying, but luckily also quite easy to fix.
- open the start screen
- type default and press enter (it should open default programs)
- choose the top option (Set your default programs)
- if you followed my advice with ninite you can use the following steps, if not you'll have to figure out your config yourself.
- choose Google Chrome in the left list, and click "Set his program as default" button in the bottom of the screen
- do the same for VLC media player & Windows Photo Viewer  


Unfortunately my PDF-viewer of choice (Foxit Reader) doesn't add itself to the list of programs, so we'll have to set up that association manually.
- search for a pdf-file
- right click it and choose __Open with__ and __Choose default program...__
- click Foxit reader in the list that now pops up

## Change display language of Windows 8
One of the greatest new features is the ease with which you can change the display language. Now I can install and setup a pc using English (my preferred language when installing) and change the language to Dutch with a few steps.
- search for language in the start screen and click __Settings__ in the top right
- click the language tile
- choose the __Add a language__ button and pick the language you'd like to add
- now choose the __Options__ of the language you added
- start the __Download and install language pack__ routine by clicking the button
- follow the prompts and your pc will now be the language of your choice
