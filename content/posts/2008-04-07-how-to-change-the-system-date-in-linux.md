---
title: How to change the system date in Linux
author: Danesh Manoharan
date: 2008-04-07T13:32:40+00:00
pvc_views:
  - 32988
dsq_thread_id:
  - 889732279

---
A friend needed help changing the system date on his Linux box today. This is usually a simple task for Linux users but newbies tend to get confused by the `"date [-u|--utc|--universal] [MMDDhhmm[[CC]YY][.ss]]"` line in the man page.

To simplify, this is how you do it.

Set the current date to April 7 2008 8:42:45pm.

The easy way,

`#date -s "7 April 2008 20:42:45"`

The harder way,

`#date  040720422008.45`

The break down: MM DD hh mm YYYY ss

MM = month = 04

DD = day = 07

hh = hour = 20

mm = minute = 42

YYYY = year = 2008

ss = second = 450

<!--more-->

sample output,

`[root@klmsyslog01p ~]# date -s "7 April 2008 20:42:45"<br />
Mon Apr  7 20:42:45 MYT 2008<br />
[root@klmsyslog01p ~]#`

`[root@kmmserver01p ~]# date 040720422008.45<br />
Mon Apr  7 20:42:45 MYT 2008<br />
[root@kmmserver01p ~]#`