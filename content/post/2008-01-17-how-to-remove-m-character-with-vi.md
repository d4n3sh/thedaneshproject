---
title: How to remove ^M character with VI
author: Danesh
date: 2008-01-17T09:09:05+00:00
url: /posts/how-to-remove-m-character-with-vi/
pvc_views:
  - 86698
dsq_thread_id:
  - 889802409

---
This is how you remove those annoying ^M characters that show up in files previously edited on a Windows/DOS platform.

In VI,

    :%s/[ctrlkey+v and ctrl-key+M]//g

actual command,

    :%s/^V^M//g

Here&#8217;s a walk through video I made. My first actually 🙂

[youtube]http://www.youtube.com/watch?v=Fy_w3VDkxKU[/youtube]