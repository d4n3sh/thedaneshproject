---
title: 'Archlinux: Can’t find ifconfig'
author: Danesh Manoharan
date: 2013-06-10T14:23:43+00:00
---
![archlinux-logo](/wp-content/uploads/2013/06/archlinux-logo-450x450.jpg)

Archlinux dropped support for ifconfig "net-tools" sometime back. [[announcement][2]]

To get the ip address use "ip" tool instead.

ip addr show dev [device name]

`ip addr show dev enp2s0`

If you really want ifconfig back then grab the "net-tools from the AUR.

 [1]: /wp-content/uploads/2013/06/archlinux-logo.jpg
 [2]: https://www.archlinux.org/news/deprecation-of-net-tools/
