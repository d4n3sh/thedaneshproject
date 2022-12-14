---
title: How to install GScrot – Screenshot Tool
author: Danesh Manoharan
date: 2009-01-17T08:47:05+00:00
pvc_views:
  - 7850
robotsmeta:
  - index,follow
dsq_thread_id:
  - 894698778

---
![](/wp-content/uploads/2009/01/gscrot064-500x400.png)

Update [Â  Feb 16 2009 ] - [GScrot has been renamed to Shutter][1].

[GScrot][2] is a popular screen-shot tool for Linux. GScrot is currently at version 0.64. It runs best on GNOME and has a good feature list.

  * Capture a website, whole desktop, individual window or a custom selection.
  * Support for delayed screen-shots.
  * Plug-ins for multiple effects.
  * Support for FTP uploads and image hosting services. imageshack.us, imagebanana.com and ubuntu-pics.de.
  * Save your screen-shots in the same folder everytime and automatically name them.
  * Full intergration with GNOME desktop panel.
  * Automatically generate thumbnails
  * Built in image editing tool.

I'll walk you through the process of installing GScrot on Ubuntu 8.10. I'm more of a command line guy so if you need a GUI version [look here][3].

Create a new apt-repository source file. I'll call itÂ  gscrot.list and place it in the "/etc/apt/source.list.d/" directory.

Add the following lines to the /etc/apt/source.list.d/gscrot.list file you just created.

`deb http://ppa.launchpad.net/gscrot/ubuntu intrepid main<br />
deb-src http://ppa.launchpad.net/gscrot/ubuntu intrepid main`

Next, run "apt-get update" to update the apt-repository database.

`root@python:/etc/apt/sources.list.d# apt-get update`

Run "apt-get install gscrot" to download and install GScrot.

`root@python:/etc/apt/sources.list.d# apt-get install gscrot`

To start GScrot, go to Applications -> Accessories -> GScrot

 [1]: /posts/cscrot-is-now-shutter/
 [2]: http://gscrot.ubuntu-projekte.de/
 [3]: http://gscrot.ubuntu-projekte.de/?page_id=243