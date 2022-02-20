---
title: How to configure a static ip in Linux
author: Danesh
date: 2008-06-16T14:56:20+00:00
url: /posts/how-to-configure-a-static-ip-in-linux/
pvc_views:
  - 71614
dsq_thread_id:
  - 889819712

---
This is a newbie question I get quite often.

Configuring your Linux machine to run on a static IP is easy. Tools like system-config-network and netconfig provide you simple GUIs to do this.

For today, I&#8217;ll show you how to do this from the command line instead.

Navigate to /etc/sysconfig/network-scripts/  
`<br />
[root@baboo]# cd /etc/sysconfig/network-scripts/`

Every network interface will have it&#8217;s own interface script file. eth0,eth1,eth2 and so on. Vi the ifcfg-eth0 interface script file for interface eth0. Replace the contents of the ifcfg-eth0 file with the parameters below.

`[root@baboo]# vi ifcfg-eth0.`  
`<br />
DEVICE=eth0<br />
TYPE=Ethernet<br />
ONBOOT=yes<br />
BOOTPROTO=none<br />
IPADDR=192.168.0.100<br />
NETMASK=255.255.255.0<br />
GATEWAY=192.168.0.1<br />
HWADDR=00:0F:22:71:0A:53<br />
USERCTL=no<br />
USERCTL=no`

If you want to switch back to DHCP, repeat the steps above and replace the contents of the ifcfg-eth0 file with the parameters below.

`DEVICE=eth0<br />
BOOTPROTO=dhcp<br />
HWADDR=00:0F:20:71:0A:50<br />
ONBOOT=yes<br />
TYPE=Ethernet<br />
DHCP_HOSTNAME=klmdrpdr01p.klm1.netcel360.com`

Restart your interface to apply the changes.  
`<br />
[root@baboo]#ifdown eth0<br />
[root@baboo]#ifup eth0`

To update your dns server settings, modify the /etc/resolv.conf.

`[root@baboo]# vi /etc/resolv.conf`

Replace the contents of the resolv.conf file with the parameters below. The first parameter &#8220;search&#8221; is your search path followed the nameserver parameters which hold the IPs for your primary and secondary DNS servers.  
`<br />
search example.com<br />
nameserver 192.168.0.5<br />
nameserver 192.168.0.6`

That&#8217;s it. Drop me a note if you need any help.