---
title: How to disable cnfs in GPFS
author: Danesh
date: 2016-11-11T08:44:04+00:00
url: /posts/how-to-disable-cnfs-in-gpfs/
dsq_thread_id:
  - 5295593831

---
Review your current cnfs setup.

<pre class="theme:shell-default lang:sh decode:true">mmlscluster --cnfs</pre>

Delete the nodes returned from the previous command from your cnfs configuration.

<pre class="theme:shell-default lang:sh decode:true">mmchnode --cnfs-interface=DELETE -N foonsd1,foonsd2</pre>

Verify cnfs has been disabled.

<pre class="theme:shell-default lang:sh decode:true">mmlscluster --cnfs</pre>

&nbsp;