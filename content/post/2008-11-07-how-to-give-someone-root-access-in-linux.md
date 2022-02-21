---
title: How to give someone root access in Linux
author: Danesh
date: 2008-11-07T06:38:41+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 4070
dsq_thread_id:
  - 890629746

---
Giving someone root access in linux is easy. Why would someone need to be root I don&#8217;t know but this is how you do it using the usermod command.

To add root access

`[root@abika root]# id sys_admin<br />
uid=508(sys_admin) gid=508(sys_admin) groups=508(sys_admin)<br />
[root@abika root]# usermod -G root sys_admin<br />
[root@abika root]# id sys_admin<br />
uid=508(sys_admin) gid=508(sys_admin) groups=508(sys_admin),0(root)`

To remove root access.

`[root@abika root]# usermod -G sys_admin sys_admin<br />
[root@abika root]# id sys_admin<br />
uid=508(sys_admin) gid=508(sys_admin) groups=508(sys_admin)`