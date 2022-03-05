---
title: "How to obtain the EOS version on a Arista switch router"
description: "Two quick ways to obtain the EOS version running on a Arista switch router."
date: 2022-02-24T15:31:26-06:00
draft: false
tags:
- howto
- arista
cover:
    image: "Arista_Logo.png"
    alt: "Arista Logo"
    caption: "Arista Logo"
    relative: true
    hidden: false # only hide on current single page
---

Whether logging a support call or planning an upgrade, knowing your current running software version is crucial. Here's two ways to quickly get the EOS version running on your Arista switch router.

## Option 1

Use the `show version` command.

```bash
(admin@lab01.local) Password:
Last login: Thu Feb 24 15:33:07 2022 from 192.168.1.253
SW01(s1)>en
SW01(s1)#show version | grep Software
Software image version: 4.18.5M
SW01(s1)#
```

## Option 2

Use the base Linux OS

```bash
(admin@lab01.local) Password:
Last login: Thu Feb 24 15:33:07 2022 from 192.168.1.253
SW01(s1)>en
SW01(s1)#bash

Arista Networks EOS shell

[admin@SW01 ~]$ cat /etc/system-release
Arista Networks EOS 4.18.5M
SW01(s1)#
```
