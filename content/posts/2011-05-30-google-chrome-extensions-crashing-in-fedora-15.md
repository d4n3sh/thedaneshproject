---
title: Google Chrome extensions crashing in Fedora 15
author: Danesh Manoharan
date: 2011-05-30T03:43:53+00:00
tags:
- linux
---
![](/wp-content/uploads/2011/05/chrome-error-f15-450x106.png)

Many have been complaining of their chrome extensions crashing in Fedora 15. In my case it was LastPass and Xmarks.

The issue is caused by SELinux and the quick fix is to disable SELinux. Here's how you get it done;

1. Fire up a terminal

2. cd to /etc/selinux/

3. vi the "config" file.

4. Change "SELINUX=enforcing" to "SELINUX=disabled"

5. Reboot, launch Chrome and your extensions should be working fine.
