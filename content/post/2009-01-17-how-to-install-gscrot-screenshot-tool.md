---
title: How to install GScrot – Screenshot Tool
author: Danesh
date: 2009-01-17T08:47:05+00:00
pvc_views:
  - 7850
robotsmeta:
  - index,follow
dsq_thread_id:
  - 894698778

---
<img loading="lazy" class="alignnone size-medium wp-image-1148" title="gscrot064" src="/wp-content/uploads/2009/01/gscrot064-500x400.png" alt="gscrot064" width="500" height="400" srcset="/wp-content/uploads/2009/01/gscrot064-500x400.png 500w, /wp-content/uploads/2009/01/gscrot064.png 669w" sizes="(max-width: 500px) 100vw, 500px" />

Update [Â  Feb 16 2009 ] &#8211; [GScrot has been renamed to Shutter][1].

[GScrot][2] is a popular screen-shot tool for Linux. GScrot is currently at version 0.64. It runs best on GNOME and has a good feature list.

  * Capture a website, whole desktop, individual window or a custom selection.
  * Support for delayed screen-shots.
  * Plug-ins for multiple effects.
  * Support for FTP uploads and image hosting services. imageshack.us, imagebanana.com and ubuntu-pics.de.
  * Save your screen-shots in the same folder everytime and automatically name them.
  * Full intergration with GNOME desktop panel.
  * Automatically generate thumbnails
  * Built in image editing tool.

I&#8217;ll walk you through the process of installing GScrot on Ubuntu 8.10. I&#8217;m more of a command line guy so if you need a GUI version [look here][3].

Create a new apt-repository source file. I&#8217;ll call itÂ  gscrot.list and place it in the &#8220;/etc/apt/source.list.d/&#8221; directory.

Add the following lines to the /etc/apt/source.list.d/gscrot.list file you just created.

`deb http://ppa.launchpad.net/gscrot/ubuntu intrepid main<br />
deb-src http://ppa.launchpad.net/gscrot/ubuntu intrepid main`

Next, run &#8220;apt-get update&#8221; to update the apt-repository database.

`root@python:/etc/apt/sources.list.d# apt-get update`

Run &#8220;apt-get install gscrot&#8221; to download and install GScrot.

`root@python:/etc/apt/sources.list.d# apt-get install gscrot`

To start GScrot, go to Applications &#8211;> Accessories &#8211;> GScrot

 [1]: /posts/cscrot-is-now-shutter/
 [2]: http://gscrot.ubuntu-projekte.de/
 [3]: http://gscrot.ubuntu-projekte.de/?page_id=243