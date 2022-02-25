---
title: Remove Zenworks Management Daemon
author: Danesh
date: 2007-08-21T03:20:14+00:00
pvc_views:
  - 5717
dsq_thread_id:
  - 905240038

---
[![opensuse-friendly.png][1]][2]

openSUSE is an awesome OS but has a few annoyance. We will look at the Zenworks Management Daemon today. Somehow every time I install or update a package through YaST or the updater the the process will stall at "synchronizing with Zen" or something like that.

I am not the first person to face this problem so hopefully openSUSE 10.3 which is coming out soon will address this.

Follow the steps below to remove ZMD,

> #> sudo su &#8211;
> 
> #> rczmd stop
> 
> #> rpm -e zmd libzypp-zmd-backend sqlite-zmd rug zen-updater

Ok, now the built in openSUSE updater will kick in the next time you run an update.

 [1]: /wp-content/uploads/2007/08/opensuse-friendly.png
 [2]: /wp-content/uploads/2007/08/opensuse-friendly.png "opensuse-friendly.png"