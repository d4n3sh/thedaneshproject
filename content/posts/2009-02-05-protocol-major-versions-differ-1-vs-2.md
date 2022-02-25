---
title: 'Protocol major versions differ: 1 vs. 2'
author: Danesh Manoharan
date: 2009-02-05T01:50:59+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 21668
dsq_thread_id:
  - 889867594

---
Protocol major versions differ: 1 vs. 2.Â 

The error above normally comes up when you try to ssh into a machine which has it's allowed ssh protocol versions locked down to a single version, today it's normally version 2.

In the /etc/ssh/sshd_config file there's a "Protocol" parameter which governs the allowed protocol version. It's normally set to "2" for better security today.

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