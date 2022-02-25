---
title: 'Linux Tip #5: Reload you /etc/inittab file'
author: Danesh Manoharan
date: 2009-04-14T11:19:10+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 6497
dsq_thread_id:
  - 889816211

---
You made changes to your /etc/inittab file but can't effort any downtime. 

There's a simple trick to reload and apply changes in your /etc/inittab file without a reboot.

Run "init q" or "init Q"

`[root@snoopy ~]# init q<br />
[root@snoopy ~]#<br />
[root@snoopy ~]# init Q<br />
[root@snoopy ~]#<br />
`