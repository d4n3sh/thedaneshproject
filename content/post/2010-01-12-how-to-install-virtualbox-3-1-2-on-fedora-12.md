---
title: How to install VirtualBox 3.1.2 on Fedora 12
author: Danesh
date: 2010-01-11T17:45:29+00:00
url: /posts/how-to-install-virtualbox-3-1-2-on-fedora-12/
pvc_views:
  - 6806
dsq_thread_id:
  - 890182021

---
<img loading="lazy" class="alignnone size-full wp-image-1953" title="vbox_logo2_gradient" src="/wp-content/uploads/2010/01/vbox_logo2_gradient.png" alt="" width="140" height="180" />

Here&#8217;s a quick guide to install [VirtualBox][1] 3.1.2 on Fedora 12

1. Import Sun&#8217;s public key

`[dexter]# wget -q http://download.virtualbox.org/virtualbox/debian/sun_vbox.asc -O- | rpm --import -`

2. Download the Fedora repo file and save it into the /etc/yum.repos.d/ directory

`[dexter]# cd /etc/yum.repos.d/`

`[dexter]# wget http://download.virtualbox.org/virtualbox/rpm/fedora/virtualbox.repo`

`[dexter]# yum clean all`

3. Install VirtualBox 3.1.2

`[dexter]# yum install VirtualBox-3.1`

That&#8217;s it!

 [1]: http://www.virtualbox.org/wiki/Linux_Downloads