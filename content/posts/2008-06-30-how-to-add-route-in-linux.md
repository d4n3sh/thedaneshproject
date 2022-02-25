---
title: How to add route in Linux
author: Danesh
date: 2008-06-30T08:53:23+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 122713
dsq_thread_id:
  - 889808269

---
To view the current routing table run &#8220;_**route -n**_&#8221;

`[root@klmppswdr01p ~]# route -n<br />
Kernel IP routing table<br />
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface<br />
10.41.42.0      0.0.0.0         255.255.255.0   U     0      0        0 eth0<br />
10.41.41.0      10.41.42.8      255.255.255.0   UG    0      0        0 eth0<br />
169.254.0.0     0.0.0.0         255.255.0.0     U     0      0        0 eth0<br />
0.0.0.0         10.41.42.1      0.0.0.0         UG    0      0        0 eth0`

To add a route refer to the command below.

`"route add -net 10.41.41.0 netmask 255.255.255.0 gw 10.41.42.8"`

To delete a route refer to the command below.

`"route del -net 10.41.41.0 netmask 255.255.255.0 gw 10.41.42.8"`

The routing information above is not persistent across reboots. After a reboot, the routing information will be lost and you need to add them in again.

To make the routing information persistent, add the &#8220;_**route add**_&#8221; line as seen above into the **_/etc/rc.local_** file.

Sample _**/etc/rc.local**_ file.

`#!/bin/sh<br />
#<br />
# This script will be executed *after* all the other init scripts.<br />
# You can put your own initialization stuff in here if you don't<br />
# want to do the full Sys V style init stuff.<br />
touch /var/lock/subsys/local<br />
route add -net 10.41.41.0 netmask 255.255.255.0 gw 10.41.42.8`