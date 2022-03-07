---
author: "Danesh Manoharan"
title: "Arista EOS: Management Interface IP"
date: 2022-03-07T09:26:52-06:00
description: "Assign management interface IP address on a Arista switch" # Post description, shows up below title
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: true # when using page bundles set this to true
    hidden: true # only hide on current single page
images:
- 
tags:
- howto
- arista
type: post
lastmod: 2022-03-07T09:26:52-06:00
draft: false
---
Follow the steps below to assign or change the IP address on the management interface on a Arista swtich.

```text
localhost> en
localhost# configure
localhost(config)# interface management 1
localhost(config-if-Ma1)# ip address 192.168.57.2/24
localhost(config-if-Ma1)# show active
interface Management 1
    ip address 192.168.57.2/24
localhost(config-if-Ma1)# exit
localhost(config)# exit
localhost# copy running-config startup-config
```
