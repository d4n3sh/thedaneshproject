---
title: How to install Google Music Manager on Fedora 16
author: Danesh Manoharan
date: 2011-11-17T14:28:28+00:00
pvc_views:
  - 5527
dsq_thread_id:
  - 889900534

---
![](/wp-content/uploads/2011/11/Google-Music-Icon-150x150.png)

I've been using Google's Music locker / streaming service for awhile now. You get to upload 20,000 tracks and getting them on is a breeze with Google's Music Manager. I'm running Fedora 16 now and here's I got Google Music Manager running on it.

1. Get into your home downloads directory.  
`# cd ~/Downloads<br />
` 2. Download the Google Music Manager rpm.  
64bit:  
`# wget http://dl.google.com/linux/direct/google-musicmanager-beta_current_x86_64.rpm<br />
` 32bit:  
`# wget http://dl.google.com/linux/direct/google-musicmanager-beta_current_i386.rpm<br />
`  
3. Satisfy the dependencies. Install the qt-x11 package.  
`# sudo yum install qt-x11<br />
` 4. Install the Google Music Manager package.  
`# sudo yum localinstall google-musicmanager-beta_current_x86_64.rpm<br />
`  
Possible error; make sure you have qt-x11 installed.  
`[danesh@pandora ~]$ google-musicmanager<br />
/usr/bin/google-musicmanager: error while loading shared libraries: libQtGui.so.4: cannot open shared object file: No such file or directory`