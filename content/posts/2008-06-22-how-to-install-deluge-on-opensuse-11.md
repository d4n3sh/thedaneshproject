---
title: How to install Deluge on openSUSE 11
author: Danesh Manoharan
date: 2008-06-22T11:22:48+00:00
pvc_views:
  - 9671
dsq_thread_id:
  - 891521614

---
![](/wp-content/uploads/2008/06/deluge.png)

Check is the Deluge package is available.  
`pandora:~ # zypper se deluge`

Install Deluge  
`pandora:~ # zypper in deluge`  
<!--more-->Here's my screen dump;

`pandora:~ # zypper se deluge<br />
Reading installed packages...`

S | Name | Summary | Type  
-+——————-+————————————-+——-  
| deluge | Bittorrent Client | package  
| deluge-debuginfo | Debug information for package deluge | package  
| deluge-debugsource | Debug sources for package deluge | package  
pandora:~ # zypper in deluge  
Reading installed packages...

The following NEW packages are going to be installed:  
deluge python-pyxdg python-orbit python-gnome-extras python-gnome  
mozilla-xulrunner181 libxml2-python libgda-3\_0-sqlite libgda-3\_0-postgres  
libgda-3\_0-mysql libgda-3\_0 libgda-3_0-3 libgda gtkspell dbus-1-python boost

Overall download size: 10.0 M. After the operation, additional 41.6 M will be used.  
Continue? [YES/no]: yes

Downloading package deluge-0.5.9.1-0.pm.1.i586 (16/16), 1.9 M (6.6 M unpacked)  
Downloading: deluge-0.5.9.1-0.pm.1.i586.rpm [done (17.1 K/s)]  
Installing: deluge-0.5.9.1-0.pm.1 [done]

 [1]: /wp-content/uploads/2008/06/deluge.png)