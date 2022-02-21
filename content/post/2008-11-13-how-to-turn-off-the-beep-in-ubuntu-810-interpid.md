---
title: How to turn off the beep in Ubuntu 8.10 Interpid
author: Danesh
date: 2008-11-13T02:29:23+00:00
pvc_views:
  - 4439
robotsmeta:
  - index,follow
dsq_thread_id:
  - 906212722

---
Hate the damn beep? Let&#8217;s get rid of it!!

Run &#8220;**lsmod**&#8221; and look for pcspkr.

If you find it then run &#8220;**rmmod pcspkr**&#8220;.

Also, make sure to add this line to your **&#8220;/etc/modprobe.d/blacklist&#8221;** file to make the change is persistent accross reboots.

`#Remove beeping speaker<br />
blacklist pcspkr`

Output;

`[root@dingo ~]# lsmod | grep pcspkr<br />
[root@dingo ~]# echo "blacklist pcspkr" >> /etc/modprobe.d/blacklist<br />
[root@dingo ~]# sudo rmmod pcspkr`