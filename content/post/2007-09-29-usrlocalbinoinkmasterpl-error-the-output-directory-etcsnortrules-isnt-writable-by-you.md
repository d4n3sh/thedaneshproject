---
title: '/usr/local/bin/oinkmaster.pl: Error: the output directory “/etc/snort/rules” isn’t writable by you.'
author: Danesh
date: 2007-09-29T08:21:12+00:00
url: /posts/usrlocalbinoinkmasterpl-error-the-output-directory-etcsnortrules-isnt-writable-by-you/
pvc_views:
  - 8170
dsq_thread_id:
  - 893025136

---
I recently upgrade my [IPCop][1] to version 1.4.16 but my Snort (Intrusion Detection System) failed to load the latest rules set. The install logs revealed the error below.

> /usr/local/bin/oinkmaster.pl: Error: the output directory &#8220;/etc/snort/rules&#8221; isn&#8217;t writable by you.

The fix was simple. simply change the permission for the &#8220;/etc/snort/rules&#8221; folder so that the owner is &#8220;snort&#8221; using the command below.

> \# chown -R snort:snort /etc/snort/rules  
> \# ls -l /etc/snort/ | grep drw  
> drwxr-xr-x 2 snort snort 4096 2007-09-18 18:20 rules

 [1]: http://www.ipcop.org/