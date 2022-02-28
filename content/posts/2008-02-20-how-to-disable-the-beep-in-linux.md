---
title: How to disable the beep in Linux
author: Danesh Manoharan
date: 2008-02-19T16:54:01+00:00
pvc_views:
  - 26564
dsq_thread_id:
  - 889892963

---
![](http://img523.imageshack.us/img523/975/startupbeepsoz2.gif)

If you are like me then you must hate the "BEEP!" that comes along with Linux. Turning it off in KDE or Gnome is easy but what if you are on the virtual console? Here's how you get rid of the "BEEP!" temporarily or permanently.

_**Temporary solution,**_

\*\* make sure to be root or use sudo \*\*

1. Check if you have the pcspkr module loaded.

```
[root@nosebleed ~]# lsmod | grep pcspkr

pcspkr                  7105  0
```

2. Remove the module. lsmod will return nothing if the module was removed.

```
[root@nosebleed ~]# rmmod pcspkr

[root@nosebleed ~]# lsmod | grep pcspkr
```

3. Restore the module when done.

```
[root@nosebleed ~]# modprobe pcspkr

[root@nosebleed ~]# lsmod | grep pcspkr

pcspkr                  7105  0
```

_**Permanent solution,**_

\*\* make sure to be root or use sudo \*\*

1. add the pcspkr module to the modprobe blacklist file.

```
[root@nosebleed ~]# vi /etc/modprobe.d/blacklist
```

Add the lines below to the file.

```
# pcspkr - turn off pc speaker "BEEP!"

blacklist pcspkr
```

2. Reboot, and check if the pcspkr module was loaded. If the blacklist file kicked in then nothing will be returned.

```
[root@nosebleed ~]# lsmod | grep pcspkr
```

This fix works for my CentOS and Ubuntu but not openSUSE as the pcspkr driver is built right into the kernel.