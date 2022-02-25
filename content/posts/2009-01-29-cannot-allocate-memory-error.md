---
title: cannot allocate memory error
author: Danesh
date: 2009-01-29T15:55:04+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 12908
dsq_thread_id:
  - 889757910

---
Had a weird memory error my Linux servers at work today. These were heavy duty machines runningÂ  heavy jobs throughout the day. /var/log/messages kept reporting that the kernel had no more memory to process new jobs. Most of the errors read &#8221; cannot allocate memory &#8221;

Some digging around later we found the fix. Kernel 2.6 has a new parameter &#8220;min\_free\_kbytes&#8221; which allows it to reserve a dedicated amount of memory for itself to process jobs. This kept the kernel from choking up when the servers were faced with sudden spikes in heavy jobs.

I set my server'sÂ  &#8220;min\_free\_kbytes&#8221; to &#8220;4096&#8221; kbytes which was the recommended value. It's more of a trial and error configuration so I'll have to monitor the server over a period of time and increase the value if needed till I hit the sweet spot.

How to set it?

To have the new value take effect immediately, edit the &#8220;/proc/sys/vm/min\_free\_kbytes&#8221; file. Remember!, reboot and the changes will be forgotten.

`echo "4096" > /proc/sys/vm/min_free_kbytes`

To have it permanent, add &#8220;vm.min\_free\_kbytes=65536&#8221; to the /etc/sysctl.conf file.

`echo "vm.min_free_kbytes=4096" >> /etc/sysctl.conf`