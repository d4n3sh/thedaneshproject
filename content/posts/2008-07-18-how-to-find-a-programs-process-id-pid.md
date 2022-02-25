---
title: How to find a program’s process id (pid)
author: Danesh Manoharan
date: 2008-07-18T15:36:58+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 15481
dsq_thread_id:
  - 889822770

---
Here's an easy way to get the pid of a running process.

Running the "pidof" command will return the pid(s) for a running program. See sample below,

`danny@pandora:~> pidof syslog-ng<br />
2043<br />
danny@pandora:~> pidof acpid<br />
2045<br />
danny@pandora:~> pidof /usr/bin/firefox<br />
14408<br />
danny@pandora:~> pidof /usr/bin/compiz<br />
27164<br />
danny@pandora:~> pidof /bin/bash<br />
27011 17339 16792 16477 15151 14403`

Simple right!?