---
title: How to change the hostname in Linux
author: Danesh
date: 2007-06-25T20:50:24+00:00
pvc_views:
  - 2917
dsq_thread_id:
  - 904554911

---
Changing your Linux machine's hostname is easy. Just follow the steps below.

**_root# hostname [new-host-name]_**

**_root# vi /etc/sysconfig/network_**

HOSTNAME=[new-host-name]

**_root# vi /etc/hosts_**

Make sure your new host is updated in the hosts file.

**_root# service network restart_**

Done!!