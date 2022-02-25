---
title: Change MTU on Proxmox backup server
author: Danesh Manoharan
date: 2022-02-13T19:24:06+00:00
publishdate: 2022-02-13
lastmod: 2022-02-13
draft: false
tags: [proxmox]
categories: []
---

1. Edit the `/etc/network/interfaces` file. Add `mtu 9000` to the interface.

```bash
iface lo inet loopback

auto enp4s0
iface enp4s0 inet static
        address 172.22.36.146/20
        gateway 172.22.47.254
        mtu 9000

iface enp5s0 inet manual
```

2. Restart the interface

```bash
root@hpvebkpdev01:~# systemctl restart networking.service 

root@pvebkpdev01:~# systemctl status networking.service 
? networking.service - Network initialization
     Loaded: loaded (/lib/systemd/system/networking.service; enabled; vendor preset: enabled)
     Active: active (exited) since Sun 2022-02-13 13:03:11 CST; 14s ago
       Docs: man:interfaces(5)
             man:ifup(8)
             man:ifdown(8)
    Process: 2052 ExecStart=/usr/share/ifupdown2/sbin/start-networking start (code=exited, status=0/SUCCESS)
   Main PID: 2052 (code=exited, status=0/SUCCESS)
        CPU: 476ms

Feb 13 13:03:10 pvebkpdev01 systemd[1]: Starting Network initialization...
Feb 13 13:03:10 pvebkpdev01 networking[2052]: networking: Configuring network interfaces
Feb 13 13:03:11 pvebkpdev01 systemd[1]: Finished Network initialization.

root@pvebkpdev01:~# ip a list enp4s0
2: enp4s0: &lt;BROADCAST,MULTICAST,UP,LOWER_UP&gt; mtu 9000 qdisc mq state UP group default qlen 1000
    link/ether 00:07:43:05:b9:f4 brd ff:ff:ff:ff:ff:ff
    inet 172.20.32.146/20 scope global enp4s0
       valid_lft forever preferred_lft forever
    inet6 fe80::207:43ff:fe05:b9f4/64 scope link 
       valid_lft forever preferred_lft forever
```
