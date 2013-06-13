---
layout: post
title: "password management for geeks"
description: "what you can do when you don't trust third parties with your passwords"
category:
tags: ["passwords", "encryption", "vim", "google drive", "dropbox"]
---
{% include JB/setup %}

## The answer to all our questions: vim
Since I started using vim mode in Komodo Edit 2 years ago I have become a vim enthusiast. This probably is the first editor I ever used where the actions I want to take are coupled with the actions that are easily available. But this isn't about vim, it's about password management.
This guide assumes you are already proficient in vim, if you are not, you probably shouldn't follow this guide.

# My setup
I have a Macbook Air at home, use a Windows 8 laptop at work and use a Nexus 4 (android) device when I'm not at work or at home. I have installed macvim on the mac, gvim on the windows laptop and vim on my Nexus 4. All of these seem to support the encrypt functionality that is included in vim 7.3. Vim uses [blowfish encryption](http://en.wikipedia.org/wiki/Blowfish_%28cipher%29), which probably isn't the most secure there is, but it is open source, freely usable and contains no real known vulnerabilities (even though it has been around for at least a decade). Furthermore, because it is open source and implemented in vim, I can be pretty sure that the NSA hasn't implemented some back doors in it.  
I use Google Drive to synchronize my document across several computers. But you can also use DropBox, or if you don't trust Google with your encrypted documents you could probably save it on a flash drive or perhaps in a VPS (with the added benefit that you can use it on your VPS). 

# The encryption
To create your password file it is important that you first prevent vim from creating some backup & temporary files. Because you really don't want the unencrypted file to be stored anywhere, ever.  
Add these lines to your vimrc:

    set nobackup
    set noswapfile
    set nowritebackup

This prevents vim from creating a swap file (live copy of what you are currently editing written to disk) and prevents vim from creating backup files. I have these options turned off anyway, because I don't like the litter they create.

Next step is to create a .txt file in a place of your choice and to open it with vim. I have made it in a folder of Google Drive that is shared between my work account and my personal account to make sure I can always access it.
In normal mode type (it is a capital)

    :X

Vim will now prompt you for your pass phrase, I recommend choosing a very long and hard to guess pass phrase, but you could choose 1234 if that is what you want. Now you can use any format you want for your passwords, I have made sections in my file for forums, social media, mail etc.

# Creating some shortcuts
## Android
- install [vim touch](https://play.google.com/store/apps/details?id=net.momodalo.app.vimtouch) on your Android device
- add 1x1 Google Drive widget to your homescreen and navigate to your passwords file to create a direct shortcut
- open it and select Vim Touch as your default application for these kinds of files

## Windows 8
- use [obly tile](http://forum.xda-developers.com/showthread.php?t=1899865) to create a custum tile on your start screen
- enter a tile name
- user _C:\Program Files (x86)\Vim\vim73\gvim.exe_ as your file path
- enter the path to your passwords file between quotes
- use a Tile Image of your liking, I used a [google images query](https://www.google.nl/search?q=lock&biw=1920&bih=1137&tbm=isch&source=lnt&tbs=isz:ex,iszw:120,iszh:120&sa=X&ei=dta5UbvRIcia0QXPkYDgCQ&ved=0CCgQpwUoBQ#q=lock&tbs=isz:ex,iszw:120,iszh:120,itp:clipart&tbm=isch&source=lnt&sa=X&ei=fNa5Ub3ACaeM0AW4i4CwCQ&ved=0CEAQpwUoAw&bav=on.2,or.r_qf.&bvm=bv.47883778,d.d2k&fp=6e4e04327c00ad79&biw=1920&bih=1137) to find a nice image
- add it to your start screen by pressing _Create Tile_

## os x
I am a heavy user of [Alfred](http://www.alfredapp.com/), it really is _just_ a quick launcher, but it's crazy fast, so I like it.
- I use cmd+space to open Alfred
- type _open &lt;filename&gt;_ and press enter
