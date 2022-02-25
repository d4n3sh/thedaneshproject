---
title: How to boot RS6000 in single user mode
author: Danesh Manoharan
date: 2007-12-16T15:15:05+00:00
pvc_views:
  - 19335
dsq_thread_id:
  - 889736931

---
We had a DC shutdown last night, been in the office for almost 20 hours now. I'm sleepy,tired,sticky,red eyedÃ‚Â and the damn 10 year old RS6000 box running AIX 4.3Ã‚Â decided to stay down.

The box was trying to connect to aÃ‚Â NFS share on the network before the network services came up. This cause the RS6000 to stall at boot up.

The fix the below fixed the problem.

  1. Restart the machine.
  2. Wait the the AIX splash screen to come up. Devices begin to initialize here.
  3. When you see the [keyboard] word on screen hit the F5 button or the 5 key depending on your console.
  4. Choose "single user mode" when the maintenance screen comes up.
  5. Edit the /etc/filesystems file and remove the NFS entries.
  6. Reboot.

Hitting F1 or the 1 key will take you to the SMS (System Management Services)Ã‚Â menu where you can access system configurations liek the network settings, boot sequence, firmware update and others....

Source: [Sys Admin Pocket Survival Guide][1]

 [1]: http://www.cs.fiu.edu/~tho01/psg/aix.html