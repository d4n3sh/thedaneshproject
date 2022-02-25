---
title: How to turn off the beep in Ubuntu 8.10 Interpid
author: Danesh Manoharan
date: 2008-11-13T02:29:23+00:00
pvc_views:
  - 4439
robotsmeta:
  - index,follow
dsq_thread_id:
  - 906212722

---
Hate the damn beep? Let's get rid of it!!

Run "**lsmod**" and look for pcspkr.

If you find it then run "**rmmod pcspkr**".

Also, make sure to add this line to your **"/etc/modprobe.d/blacklist"** file to make the change is persistent accross reboots.

`#Remove beeping speaker<br />
blacklist pcspkr`

Output;

`[root@dingo ~]# lsmod | grep pcspkr<br />
[root@dingo ~]# echo "blacklist pcspkr" >> /etc/modprobe.d/blacklist<br />
[root@dingo ~]# sudo rmmod pcspkr`