---
title: How can non root users mount and unmount in Linux
author: Danesh
date: 2012-07-24T15:08:25+00:00
url: /posts/how-can-non-root-users-mount-and-unmount-in-linux/
pvc_views:
  - 1193
dsq_thread_id:
  - 891607998

---
File systems / partitions are normally managed by root and only root would be able to mount or un-mount.

However, if you want everyone on your machine to have the same&nbsp;privilege for a specific mount point, this is&nbsp;how&nbsp;you can&nbsp;do&nbsp;that.

Add &#8220;**user**&#8221; to the mount options for the desired mount point in your /etc/fstab file. In my case &#8220;/media/music&#8221;

I changed mine from

`//192.168.1.200/Music /media/music rw,noauto 0 0<br />
`  
to

`//192.168.1.200/Music /media/music cifs user,rw,noauto 0 0<br />
`