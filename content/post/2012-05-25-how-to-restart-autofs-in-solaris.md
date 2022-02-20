---
title: How to restart autofs in Solaris
author: Danesh
date: 2012-05-25T02:51:50+00:00
url: /posts/how-to-restart-autofs-in-solaris/
pvc_views:
  - 4886
dsq_thread_id:
  - 889983159

---
<a href="/posts/2373/solaris-logo/" rel="attachment wp-att-2387"><img loading="lazy" src="/wp-content/uploads/2012/02/solaris-logo.png" alt="" title="solaris logo" width="425" height="222" class="alignnone size-full wp-image-2387" /></a>

Quick step to restart the autofs service on Solaris. I&#8217;m running Solaris 10.

1. Check the auto service status.  
`# svcs | grep auto<br />
legacy_run Oct_24 lrc:/etc/rc2_d/S72autoinstall<br />
online 17:31:10 svc:/system/filesystem/autofs:default`

2. Restart the autofs service  
`# svcadm -v restart svc:/system/filesystem/autofs:default<br />
Action restart set for svc:/system/filesystem/autofs:default.`