---
title: How to restart RSH in Linux
author: Danesh
date: 2009-04-01T05:07:22+00:00
url: /posts/how-to-restart-rsh-in-linux/
robotsmeta:
  - index,follow
pvc_views:
  - 4952
dsq_thread_id:
  - 889859043

---
The [rsh][1] service is controlled by the &#8220;[xinetd][2]&#8221; super daemon. If your rsh service stops working simply run the &#8220;service xinetd restart&#8221; service to restart rsh.

Sample output;

`[root@pilon~]# service xinetd restart<br />
Stopping xinetd:                                           [FAILED]<br />
Starting xinetd:                                           [  OK  ]`

 [1]: http://en.wikipedia.org/wiki/Remote_Shell
 [2]: http://en.wikipedia.org/wiki/Xinetd