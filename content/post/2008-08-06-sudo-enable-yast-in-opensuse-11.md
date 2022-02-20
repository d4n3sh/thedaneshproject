---
title: Sudo enable Yast in openSUSE 11
author: Danesh
date: 2008-08-06T13:24:29+00:00
url: /posts/sudo-enable-yast-in-opensuse-11/
robotsmeta:
  - index,follow
pvc_views:
  - 9506
dsq_thread_id:
  - 890082087

---
One of annoyance I found on openSUSE 11 is that Yast is no longer sudo enabled. The privilege elevation sudo line &#8220;**[username] ALL=(ALL) NOPASSWD: ALL**&#8221; works with everything else except for Yast.

In versions prior to openSUSE 11 sudo worked fine with Yast. Apparently in openSUSE 11 Yast sudo was switched to su.

Here&#8217;s how you&#8217;d get Yast to start working with sudo again.

`danny@pandora:~> kwriteconfig -file kdesurc -group super-user-command -key super-user-command sudo`