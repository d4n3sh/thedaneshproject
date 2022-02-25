---
title: Installing nVidia driver on openSUSE 10.2 | Linux
author: Danesh
date: 2007-03-19T15:43:26+00:00
pvc_views:
  - 3738
dsq_thread_id:
  - 893137929

---
Installing nVidia drivers for your openSUSE 10.2

Driver Source: ftp://download.nvidia.com/opensuse/10.2/

1.start &#8211;> computers &#8211;> administrator settings &#8211;> software &#8211;> installation source  
![][1] 

<!--more-->2. Select ftp as the media type

![][2] 

3. Protocol &#8211;> ftp, server name &#8211;> download.nvidia.com, directory &#8211;> /opensuse/10.2/

![][3] 

4. Click next and probing will start

![][4] 

5. Accept the GnuPG key

![][5] 

6. Import the GnuPG key

![][5] 

![][6] 

7. Verify source is available. It should be listed as seen below.

![][7] 

8. start &#8211;> computers &#8211;> administrator settings &#8211;> software &#8211;> software management

![][8] 

9. Filter &#8211;> installation source. Select x11-video-nvidia and the appropriate kernel module.  
Run &#8220;uname -r&#8221; to get the installed kernel version.

<img loading="lazy" src="http://farm1.static.flickr.com/153/426788484_12cb5ff093.jpg?v=0" height="390" width="500" /> 

10. Accept and the install begins.

![][9] 

11. Once the installation is complete I suggest rebooting the machine. &#8220;Ctrl Backspace&#8221; will also work.

You will see an nVidia splash screen before the desktop comes up. This confirms the new nVidia drivers are loaded.

Installation instructions for other platforms are available at [here][10].

I updated my openSUSE 10.2 box at home last night after a fresh install. Too bad I'm stuck with an old 17&#8221; CRT as my LCD died. Sigh&#8230;..

 [1]: http://farm1.static.flickr.com/161/426784522_d917155812.jpg?v=0
 [2]: http://farm1.static.flickr.com/155/426784528_29fe5eaeae.jpg?v=0
 [3]: http://farm1.static.flickr.com/170/426784530_94a233b0b6.jpg?v=0
 [4]: http://farm1.static.flickr.com/161/426784533_ee894bf9f2.jpg?v=0
 [5]: http://farm1.static.flickr.com/162/426784561_a8cc6e3edf.jpg?v=0
 [6]: http://farm1.static.flickr.com/162/426788475_b1a1d84fa2.jpg?v=0
 [7]: http://farm1.static.flickr.com/178/426788477_527aeb71c7.jpg?v=0
 [8]: http://farm1.static.flickr.com/168/426788480_ec6e6a7095.jpg?v=0
 [9]: http://farm1.static.flickr.com/185/426788489_3a8ac9a9d7.jpg?v=0
 [10]: http://www.suse.de/~sndirsch/nvidia-installer-HOWTO.html#2