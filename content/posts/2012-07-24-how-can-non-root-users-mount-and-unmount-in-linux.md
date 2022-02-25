---
title: How can non root users mount and unmount in Linux
author: Danesh Manoharan
date: 2012-07-24T15:08:25+00:00
pvc_views:
  - 1193
dsq_thread_id:
  - 891607998

---
File systems / partitions are normally managed by root and only root would be able to mount or un-mount.

However, if you want everyone on your machine to have the same privilege for a specific mount point, this is how you can do that.

Add "**user**" to the mount options for the desired mount point in your /etc/fstab file. In my case "/media/music"

I changed mine from

`//192.168.1.200/Music /media/music rw,noauto 0 0<br />
`  
to

`//192.168.1.200/Music /media/music cifs user,rw,noauto 0 0<br />
`