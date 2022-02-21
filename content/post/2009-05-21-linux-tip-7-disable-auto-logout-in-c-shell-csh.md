---
title: 'Linux Tip #7: Disable auto logout in C Shell (csh)'
author: Danesh
date: 2009-05-20T18:24:10+00:00
aktt_notify_twitter:
  - no
pvc_views:
  - 11583
dsq_thread_id:
  - 889928011

---
Run the &#8220;set autologout=[n]&#8221; command to enable or disable the autologout feature in C Shell (csh)

Setting autologout to &#8220;0&#8221; will disable the autologout feature.

`set autologout=0`

The first line below will set the autologout period to 1 minute and the second line will be 5 minutes. If there is no activity for the set time, you will automatically be logged off from yoru C Shell (csh) session.

`set autologout=1`

`set autologout=5`