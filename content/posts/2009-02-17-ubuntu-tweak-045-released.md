---
title: Ubuntu Tweak 0.4.5 released!
author: Danesh
date: 2009-02-16T17:10:40+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 3820
dsq_thread_id:
  - 890055213

---
<img loading="lazy" class="alignnone size-medium wp-image-1279" title="Ubuntu Tweak 0.4.5" src="/wp-content/uploads/2009/02/ubuntu-tweak-045-500x338.png" alt="Ubuntu Tweak 0.4.5" width="500" height="338" srcset="/wp-content/uploads/2009/02/ubuntu-tweak-045-500x338.png 500w, /wp-content/uploads/2009/02/ubuntu-tweak-045.png 748w" sizes="(max-width: 500px) 100vw, 500px" />  
Ubuntu Tweak 0.4.5 is out.

Ubuntu Tweak is an application to help users easily configure their Ubuntu installation. From installing new software to cleaning up junk, Ubuntu Tweak doesÂ  it all. Ubuntu Tweak is open source and distributed under the GPL license.

I have been using Ubuntu Tweak on my Ubuntu machines at home for awhile now. When all you need is a functioning desktop then Ubuntu together with Ubuntu TweakÂ  in my book is the best choice. Not everyone fanciesÂ  the command line or editing files everytime they install new software. Especially my non IT savvy family members. Ubuntu and Ubuntu Tweak just work.

Anyway, back to Ubuntu Tweak's feature List;

* View of Basic System Information(Distribution, Kernel, CPU, Memory, etc.)  
* GNOME Session Control  
* Auto Start Program Control  
* Add / Remove software  
* Software source editor  
* 3rd party source support  
* Package cleanup  
* Show/Hide and Change Splash screen  
* Show/Hide desktop icons or Mounted Volumes  
* Show/Hide/Rename Computer, Home, Trash icon or Network icon  
* Tweak Metacity Window Managerâ€™s Style and Behavior  
* Compiz Fusion settings, Screen Edge Settings, Window Effects Settings, Menu Effect Settins  
* GNOME Panel Settings  
* Nautilus Settings  
* Advanced Power Management Settings  
* System Security Settings

The latest version has a few new features added;

* Clean old config files easily. Remove unused config files from un-installed applications.  
* Preference page to change the default Ubuntu Tweak interface.  
* Configure default application within Ubuntu Tweak. The chosen app will launch everytime Ubuntu Tweak starts.  
* All Launchpad PPA sources are now signed.  
* Change the GNOME panel logo.

ToÂ  install Ubuntu Tweak follow the steps below or download here.

1. Import the key  
`sudo apt-key adv --recv-keys --keyserver keyserver.ubuntu.com FE85409EEAB40ECCB65740816AF0E1940624A220`

2. Add the source below. My source file is &#8220;/etc/apt/sources.list.d/ubuntu-tweak.list&#8221;.

**Ubuntu 8.10 Intrepid Source:**  
`<br />
deb http://ppa.launchpad.net/tualatrix/ubuntu intrepid main<br />
deb-src http://ppa.launchpad.net/tualatrix/ubuntu intrepid main`

**Ubuntu 8.04 Hardy Source:**

`deb http://ppa.launchpad.net/tualatrix/ubuntu hardy main<br />
deb-src http://ppa.launchpad.net/tualatrix/ubuntu hardy main`

3. Run the package manager and refresh the source list when prompted. Search for Unbuntu Tweak and install it.

That's it.

Source: Ubuntu Tweak