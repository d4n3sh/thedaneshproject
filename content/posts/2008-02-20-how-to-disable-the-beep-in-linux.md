---
title: How to disable the beep in Linux
author: Danesh
date: 2008-02-19T16:54:01+00:00
pvc_views:
  - 26564
dsq_thread_id:
  - 889892963

---
<img loading="lazy" src="http://img523.imageshack.us/img523/975/startupbeepsoz2.gif" align="middle" height="263" width="196" />

If you are like me then you must hate the &#8220;BEEP!&#8221; that comes along with Linux. Turning it off in KDE or Gnome is easy but what if you are on the virtual console? Here's how you get rid of the &#8220;BEEP!&#8221; temporarily or permanently.

_**Temporary solution,**_

\*\* make sure to be root or use sudo \*\*

1. Check if you have the pcspkr module loaded.

<pre>[root@nosebleed ~]# lsmod | grep pcspkr

pcspkr                  7105  0</pre>

2. Remove the module. lsmod will return nothing if the module was removed.

<pre>[root@nosebleed ~]# rmmod pcspkr

[root@nosebleed ~]# lsmod | grep pcspkr</pre>

3. Restore the module when done.

<pre>[root@nosebleed ~]# modprobe pcspkr

[root@nosebleed ~]# lsmod | grep pcspkr

pcspkr                  7105  0</pre>

_**Permanent solution,**_

\*\* make sure to be root or use sudo \*\*

1. add the pcspkr module to the modprobe blacklist file.

<pre>[root@nosebleed ~]# vi /etc/modprobe.d/blacklist</pre>

Add the lines below to the file.

<pre># pcspkr - turn off pc speaker "BEEP!"

blacklist pcspkr</pre>

2. Reboot, and check if the pcspkr module was loaded. If the blacklist file kicked in then nothing will be returned.

<pre>[root@nosebleed ~]# lsmod | grep pcspkr</pre>

This fix works for my CentOS and Ubuntu but not openSUSE as the pcspkr driver is built right into the kernel.