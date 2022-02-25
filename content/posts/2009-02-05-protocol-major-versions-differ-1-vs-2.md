---
title: 'Protocol major versions differ: 1 vs. 2'
author: Danesh
date: 2009-02-05T01:50:59+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 21668
dsq_thread_id:
  - 889867594

---
Protocol major versions differ: 1 vs. 2.Â 

The error above normally comes up when you try to ssh into a machine which has it&#8217;s allowed ssh protocol versions locked down to a single version, today it&#8217;s normally version 2.

In the /etc/ssh/sshd_config file there&#8217;s a &#8220;Protocol&#8221; parameter which governs the allowed protocol version. It&#8217;s normally set to &#8220;2&#8221; for better security today.

Old days;

`#Protocol 2,1`

Today;

`#Protocol 2`

The ssh command allows you to specify a protocol version to use when establishing a connection.

To ssh using protocol version 1;

ssh -1 [ hostname]

`[root@abibi ~]# ssh -1 abubu`

Ro ssh using protocol version 2;

ssh -2 [ hostname]

`[root@abibi ~]# ssh -2 abubu`