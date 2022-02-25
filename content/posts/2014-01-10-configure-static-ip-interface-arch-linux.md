---
title: How to configure a static IP interface on Arch Linux
author: Danesh
date: 2014-01-10T14:58:48+00:00
dsq_thread_id:
  - 2104948257

---
<a href="/posts/configure-static-ip-interface-arch-linux/archlinux-logo-dark-1200dpi-b42bd35d5916-450x150/" rel="attachment wp-att-3419"><img loading="lazy" class="alignnone size-full wp-image-3419" alt="archlinux-logo-dark-1200dpi.b42bd35d5916-450x150" src="/wp-content/uploads/2014/01/archlinux-logo-dark-1200dpi.b42bd35d5916-450x150.png" width="450" height="150" /></a>

&nbsp;

Arch Linux defaults to DHCP on a new install. This guide will walk you through the steps need to configure a static IP interface for your Arch Linux install.

1. Create the interface config file in "/etc/netctl/". Either use the sample file in "/etc/netctl/examples/" as a base or create one from scratch. We'll create a new file for this walkthrough.

`#cd /etc/netctl<br />
#vi eth0`

The lines below go into the file.

`Description='eth0'<br />
Interface=eth0<br />
Connection=ethernet<br />
IP=static<br />
Address='192.168.1.201/24'<br />
Gateway='192.168.1.1'<br />
DNS='192.168.1.40'<br />
Broadcast='192.168.1.255'`

2. Enable the new interface.  
`#netctl enable eth0`

3. Start the new interface or reboot.  
`#netctl start eth0`