---
title: 'Archlinux: Can’t find ifconfig'
author: Danesh
date: 2013-06-10T14:23:43+00:00
url: /posts/archlinux-cant-find-ifconfig/
dsq_thread_id:
  - 1385442648

---
[<img loading="lazy" class="alignnone  wp-image-3223" alt="archlinux-logo" src="/wp-content/uploads/2013/06/archlinux-logo-450x450.jpg" width="270" height="270" srcset="/wp-content/uploads/2013/06/archlinux-logo-450x450.jpg 450w, /wp-content/uploads/2013/06/archlinux-logo-150x150.jpg 150w, /wp-content/uploads/2013/06/archlinux-logo.jpg 512w" sizes="(max-width: 270px) 100vw, 270px" />][1]

Archlinux dropped support for ifconfig &#8220;net-tools&#8221; sometime back. [[announcement][2]]

To get the ip address use &#8220;ip&#8221; tool instead.

ip addr show dev [device name]

`ip addr show dev enp2s0`

If you really want ifconfig back then grab the &#8220;net-tools from the AUR.

 [1]: /wp-content/uploads/2013/06/archlinux-logo.jpg
 [2]: https://www.archlinux.org/news/deprecation-of-net-tools/