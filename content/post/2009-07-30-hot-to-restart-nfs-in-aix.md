---
title: Hot to restart NFS in AIX
author: Danesh
date: 2009-07-30T01:21:03+00:00
aktt_notify_twitter:
  - no
pvc_views:
  - 8233
dsq_thread_id:
  - 889963655

---
Here&#8217;s a quick guide to start, stop the NFS service in AIX.

To stop the NFS service run,

`stopsrc -g nfs`

and to that the NFS service run,

`startsrc -g nfs`

To re-exports all shares or new share specified in the &#8220;exports&#8221; file run,

`exportfs -av`