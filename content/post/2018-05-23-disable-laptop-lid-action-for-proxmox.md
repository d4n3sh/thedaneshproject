---
title: Disable laptop lid action for proxmox
author: Danesh
date: 2018-05-22T22:13:31+00:00
url: /posts/disable-laptop-lid-action-for-proxmox/

---
I run a low power proxmox server using my old Lenovo T430s. It&#8217;s headless so the lid&#8217;s always closed.

When I first set it up, closing the lid would send the laptop into standby mode. Here&#8217;s what I did to get promox/debian to ignore the laptop lid action.

Edit the /etc/systemd/logind.conf file

Change the lines below.

<pre class="lang:sh decode:true">HandleLidSwitch=ignore
HandleLidSwitchDocked=ignore</pre>

restart the logind service.

<pre class="lang:sh decode:true">#systemctl restart systemd-logind.service</pre>

&nbsp;