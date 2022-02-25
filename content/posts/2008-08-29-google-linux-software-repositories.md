---
title: Google Linux software repositories
author: Danesh
date: 2008-08-29T02:00:50+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 5750
dsq_thread_id:
  - 895120770

---
Google has Linux software repositories setup for you to easily stay up to date with their Linux softwares. Their repositories supportÃ‚Â  APT, YUM, YaST, urpmi and RPM.

However, only Google Desktop and Google Picasa are published on the repositories. Google earth has to be [downloaded][1] and installed manually.

I'll show you how to add the repository in openSUSE but for other distros refer [here][2].

1. As root add the repository.

For 32 bit  
`pandora:~ # zypper sa -t YUM http://dl.google.com/linux/rpm/stable/i386 google` 

For 64 bit  
`pandora:~ # zypper sa -t YUM http://dl.google.com/linux/rpm/stable/x86_64 google64`

2. Test the repository  
`pandora:~ # zypper se picasa  </p>
<p>pandora:~ # zypper in picasa` 

Done!!

[<img class="alignnone" src="http://farm4.static.flickr.com/3006/2803064334_a402a17595_o.png" alt="" width="500" />][3]

 [1]: http://earth.google.com/
 [2]: http://www.google.com/linuxrepositories/index.html
 [3]: http://farm4.static.flickr.com/3006/2803064334_a402a17595_o.png