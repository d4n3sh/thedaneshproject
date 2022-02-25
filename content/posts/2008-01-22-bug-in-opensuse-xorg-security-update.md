---
title: Bug in openSUSE xorg security update
author: Danesh
date: 2008-01-22T12:55:00+00:00
pvc_views:
  - 10592
dsq_thread_id:
  - 894110460

---
I've been hit by [bug #345131][1] since updating to the latest xorg-server [7.2-143.9] security update on my openSUSE 10.3 installation. xorg-server version 7.2-143.6 to 7.2-143.9.

VLC, Filezilla and a few other applications stopped working. The bug has something to do with the X Window shared memory (MIT-SHM) overflowing.

My error,

> The program &#8216;Filezilla' received an X Window System error.  
> This probably reflects a bug in the program.  
> The error was &#8216;BadAlloc (insufficient resources for operation)'.  
> (Details: serial 1072 error\_code 11 request\_code 147 minor_code 5)  
> (Note to programmers: normally, X errors are reported asynchronously;  
> that is, you will receive the error a while after causing it.  
> To debug your program, run it with the -sync command line  
> option to change this behavior. You can then get a meaningful  
> backtrace from your debugger if you break on the gdk\_x\_error() function.)

Few hours of Googling and experimenting later I found my fix. 3Ã‚Â  actually.

<!--more-->1. Edit your /etc/xorg.conf file and add the below to the "Extensions" section. This fixed some issues but not all. My Kaffeine decided to stop working following this method.

Section "Extensions"  
Option "MIT-SHM" "no"  
EndSection

2. Downgrade back to the previous version [7.2-143.6] of xorg-server. This will come with quite a few dependency warnings so be prepared to work through them. Worked for me but look at option 3 as it's the best one.

3. Download and install the Beta fix xorg-server [7.2-143.10] from Novell from here. This one worked best for me.

<img loading="lazy" src="http://farm3.static.flickr.com/2085/2211346047_76d47bd0f3.jpg" height="269" width="450" /> 

Source: [Novell Bugzilla][1] SUSE Beta

 [1]: https://bugzilla.novell.com/show_bug.cgi?id=345131