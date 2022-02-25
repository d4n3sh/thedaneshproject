---
title: Linux How to change user UID and GID
author: Danesh
date: 2013-01-15T14:31:49+00:00
pvc_views:
  - 265
dsq_thread_id:
  - 1027076718

---
I was running Debian for sometime and in Debian the UID starts at 1000. Now I moved to CentOS 6 and the UID starts from 500. Simply changing the UID/GID seemed like an quick way to get my file permission back in sync.

Here&#8217;s how to easily change the UID and GID for a user in Linux. 

Check my current UID/GID  
`[root@atom ~]# id danesh<br />
uid=500(danesh) gid=500(danesh) groups=500(danesh)`

Change my UID to 1000  
`[root@atom ~]# usermod -u 1000 danesh`

Check my UID/GID again. GID is still 500.  
`[root@atom ~]# id danesh<br />
uid=1000(danesh) gid=500(danesh) groups=500(danesh)`

Change the GID for my group.  
`[root@atom ~]# groupmod -g 1000 danesh`

UID and GID now updated.  
`[root@atom ~]# id danesh<br />
uid=1000(danesh) gid=1000(danesh) groups=1000(danesh)`

This will update the files in your home directory with the correct UID/GID but anything outside you will have to do it yourself.