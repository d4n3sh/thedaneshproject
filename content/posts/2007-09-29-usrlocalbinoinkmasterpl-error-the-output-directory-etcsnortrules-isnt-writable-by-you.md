---
title: '/usr/local/bin/oinkmaster.pl: Error: the output directory “/etc/snort/rules” isn’t writable by you.'
author: Danesh Manoharan
date: 2007-09-29T08:21:12+00:00
pvc_views:
  - 8170
dsq_thread_id:
  - 893025136

---
I recently upgrade my [IPCop][1] to version 1.4.16 but my Snort (Intrusion Detection System) failed to load the latest rules set. The install logs revealed the error below.

> /usr/local/bin/oinkmaster.pl: Error: the output directory "/etc/snort/rules" isn't writable by you.

The fix was simple. simply change the permission for the "/etc/snort/rules" folder so that the owner is "snort" using the command below.

> \# chown -R snort:snort /etc/snort/rules  
> \# ls -l /etc/snort/ | grep drw  
> drwxr-xr-x 2 snort snort 4096 2007-09-18 18:20 rules

 [1]: http://www.ipcop.org/