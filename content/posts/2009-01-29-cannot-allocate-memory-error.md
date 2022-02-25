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
Had a weird memory error my Linux servers at work today. These were heavy duty machines runningÂ  heavy jobs throughout the day. /var/log/messages kept reporting that the kernel had no more memory to process new jobs. Most of the errors read " cannot allocate memory "

Some digging around later we found the fix. Kernel 2.6 has a new parameter "min\_free\_kbytes" which allows it to reserve a dedicated amount of memory for itself to process jobs. This kept the kernel from choking up when the servers were faced with sudden spikes in heavy jobs.

I set my server'sÂ  "min\_free\_kbytes" to "4096" kbytes which was the recommended value. It's more of a trial and error configuration so I'll have to monitor the server over a period of time and increase the value if needed till I hit the sweet spot.

How to set it?

To have the new value take effect immediately, edit the "/proc/sys/vm/min\_free\_kbytes" file. Remember!, reboot and the changes will be forgotten.

`echo "4096" > /proc/sys/vm/min_free_kbytes`

To have it permanent, add "vm.min\_free\_kbytes=65536" to the /etc/sysctl.conf file.

`echo "vm.min_free_kbytes=4096" >> /etc/sysctl.conf`