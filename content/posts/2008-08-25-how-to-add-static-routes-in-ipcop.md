---
title: How to add static routes in IPCop
author: Danesh
date: 2008-08-25T03:45:53+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 21564
dsq_thread_id:
  - 889778399

---
IPCop till today does not have a GUI to add static routes.

The manual method. You will have to do this every time IPCop is rebooted.

`root@proxy73:~ # route add -net 10.0.0.0 gw 10.38.24.1 netmask 255.0.0.0`

Now let's make the route persistent across reboots. There are 2 files for this. Use either one depending on your needs.

You can add the route command at the end of the **/etc/rc.d/rc.local** file. The route will be added every time IPCop is rebooted but not everytime the interface is restarted. Good for a box with minimal changes.

`root@proxy73:~ # echo "route add -net 10.0.0.0 gw 10.38.24.1 netmask 255.0.0.0" >> /etc/rc.d/rc.local`

The other way would be to add the route command at the end of the **/etc/rc.d/rc.netaddress.up** file. This will ensure that your routing table gets updated every time the interface is restarted.

`root@proxy73:~ # echo "route add -net 10.0.0.0 gw 10.38.24.1 netmask 255.0.0.0" >> /etc/rc.d/rc.netaddress.up`

I personally use the latter.

To view your routing table run the &#8220;**route**&#8221; command.

`root@proxy73:~ # route<br />
Kernel IP routing table<br />
DestinationÃ‚Â Ã‚Â Ã‚Â Ã‚Â  GatewayÃ‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  GenmaskÃ‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  Flags Metric RefÃ‚Â Ã‚Â Ã‚Â  Use Iface<br />
213.27.199.80Ã‚Â Ã‚Â  *Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  255.255.255.248 UÃ‚Â Ã‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0 eth2<br />
192.168.1.0Ã‚Â Ã‚Â Ã‚Â Ã‚Â  *Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  255.255.255.0Ã‚Â Ã‚Â  UÃ‚Â Ã‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0 eth1<br />
10.38.24.0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  *Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  255.255.248.0Ã‚Â Ã‚Â  UÃ‚Â Ã‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0 eth0<br />
10.0.0.0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  10.38.24.1Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  255.0.0.0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  UGÃ‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0 eth0<br />
defaultÃ‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  213.27.199.81Ã‚Â Ã‚Â  0.0.0.0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  UGÃ‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  0 eth2`