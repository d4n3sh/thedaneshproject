---
title: Sort files by size
author: Danesh
date: 2010-03-31T03:31:12+00:00
pvc_views:
  - 2176
dsq_thread_id:
  - 889914425

---
Here's how to sort files by size in Linux.

Standard;

`ls -lhS`

Reverse;

`ls -lhSr`

Options used;

-l &#8211;> print long listing

-h &#8211;> print human readable sizes

-S &#8211;> sort by file size

-r &#8211;> reverse order

Output;

`[root@kmon01 log]# ls -lhS<br />
total 70M<br />
-rw-r--r--  1 root     root      36M Mar 31 11:28 messages<br />
-rw-r--r--  1 root     root      15M Mar 31 11:25 cron<br />
-rw-rw-r--  1 root     root      15M Mar 31 04:02 maillog<br />
-rw-rw-r--  1 root     utmp     3.8M Mar 31 11:17 wtmp<br />
-r--------  1 root     root     2.6M Mar 31 11:17 lastlog<br />
-rw-r--r--  1 root     root     1.4M Mar 31 11:13 boot.log<br />
-rw-r--r--  1 root     root      68K Mar 25 04:04 prelink.log<br />
-rw-r--r--  1 root     root      67K May 25  2007 scrollkeeper.log<br />
-rw-r--r--  1 root     root      54K Mar 31 04:02 rpmpkgs<br />
-rw-r--r--  1 root     root      51K Dec 24  2007 xferlog<br />
-rw-r--r--  1 root     root      38K May 25  2007 anaconda.syslog<br />
-rw-r--r--  1 root     root      36K Jun 11  2007 Xorg.0.log<br />
-rw-r--r--  1 root     root      15K Feb  2 10:34 dmesg<br />
-rw-r--r--  1 root     root      13K May 25  2007 anaconda.log`

`[root@kmon01 log]# ls -lhrS<br />
total 70M<br />
-rw-r--r--  1 root     root        0 May 25  2007 spooler<br />
-rw-r--r--  1 root     root        0 Mar 25 14:38 secure<br />
-rwx------  1 postgres postgres    0 May 25  2007 pgsql<br />
-rw-r--r--  1 root     root        0 May 24  2007 mcelog<br />
-rw-r--r--  1 root     root       23 Feb  2 10:35 snmpd.log<br />
-rw-r--r--  1 root     root      715 Sep  1  2009 yum.log<br />
-rw-r--r--  1 mysql    mysql    2.0K Dec  8  2008 mysqld.log<br />
-rw-r--r--  1 root     root     2.1K Feb  2 10:35 acpid<br />
-rw-r--r--  1 root     root     2.7K Mar 22 11:46 btmp<br />
drwxr-xr-x  2 root     root     4.0K Mar 31 11:21 httpd<br />
drwxr-xr-x  2 root     root     4.0K Mar 10  2006 gdm<br />
drwxr-x---  2 exim     exim     4.0K Sep  9  2005 exim<br />
-rw-r--r--  1 root     root      67K May 25  2007 scrollkeeper.log<br />
-rw-r--r--  1 root     root      68K Mar 25 04:04 prelink.log<br />
-rw-r--r--  1 root     root     1.4M Mar 31 11:13 boot.log<br />
-r--------  1 root     root     2.6M Mar 31 11:17 lastlog<br />
-rw-rw-r--  1 root     utmp     3.8M Mar 31 11:17 wtmp<br />
-rw-rw-r--  1 root     root      15M Mar 31 04:02 maillog<br />
-rw-r--r--  1 root     root      15M Mar 31 11:25 cron<br />
-rw-r--r--  1 root     root      36M Mar 31 11:29 messages<br />
`