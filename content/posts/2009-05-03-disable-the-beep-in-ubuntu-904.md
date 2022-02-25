---
title: Disable the “beep” in Ubuntu 9.04
author: Danesh
date: 2009-05-03T03:43:56+00:00
aktt_notify_twitter:
  - no
pvc_views:
  - 10645
dsq_thread_id:
  - 895538556

---
Hate the beep? Here's how to get rid of it.

Login as "root" and run the command below.

`echo "blacklist pcspkr" >> /etc/modprobe.d/blacklist.conf`

Output;

`root@pandora:/etc/modprobe.d# echo "blacklist pcspkr" >> /etc/modprobe.d/blacklist.conf<br />
root@pandora:/etc/modprobe.d# cat /etc/modprobe.d/blacklist.conf | grep pcspkr<br />
blacklist pcspkr`