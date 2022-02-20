---
title: 'Linux Tip #5: Reload you /etc/inittab file'
author: Danesh
date: 2009-04-14T11:19:10+00:00
url: /posts/linux-tip-5-reload-you-etcinittab-file/
robotsmeta:
  - index,follow
pvc_views:
  - 6497
dsq_thread_id:
  - 889816211

---
You made changes to your /etc/inittab file but can&#8217;t effort any downtime. 

There&#8217;s a simple trick to reload and apply changes in your /etc/inittab file without a reboot.

Run &#8220;init q&#8221; or &#8220;init Q&#8221;

`[root@snoopy ~]# init q<br />
[root@snoopy ~]#<br />
[root@snoopy ~]# init Q<br />
[root@snoopy ~]#<br />
`