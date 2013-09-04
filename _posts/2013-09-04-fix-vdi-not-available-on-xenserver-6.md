---
layout: post
title: "fix vdi not available on xenserver 6"
description: "Fix 'vdi not available' error on xenserver 6"
category: 
tags: ["xen", "xenserver", "xencenter", "virtualization", "fix"]
---
{% include JB/setup %}


# A short how to to fix the annoying 'vdi not available error'
Sometimes when a VM doesn't get shut down cleanly it can generate a VDI not available error when you try to boot it. The Citrix Knowledge Center has a fix listed as [CTX138234](http://support.citrix.com/article/CTX138234). Unfortunately the last time I encountered this issue the official fix didn't work. I was able to fix the issue by moving the system disk to a different Storage Repository. This is how I did it:  
- Open up Xencenter and open the VM that gives the error
- Go to the storage tab and select the disk that gives the error (If you have only 1 disk, that's easy. If you have multiple disks, start with the smallest)
- Note the Storage Repository, it's listed in the SR column
- Click the _detach_ button and choose _yes_ 
- Navigate to the storage repo noted in the third step and search for the disk you just detached in storage tab
- Select the disk and __make sure that there is no virtual machine listed in the last column__
- Right click the disk and select _move Virtual Disk_
- Choose a storage repository from the list and click _move_ and wait for it to complete
- Select the VM that was giving you troubles and go to the storage tab
- Choose _attach disk_ and select the disk you just moved
- start the VM

In my case, this was everything I had to do to fix the error.
