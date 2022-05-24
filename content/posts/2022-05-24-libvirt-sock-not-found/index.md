---
author: "Danesh Manoharan"
title: "/usr/local/var/run/libvirt/libvirt-sock not found"
date: 2022-05-24T04:16:18-05:00
description: "/usr/local/var/run/libvirt/libvirt-sock not found on MacOS" # Post description, shows up below title
cover:
    image: "libvirtd-error-2022-05-24-04-03-36.png" # image path/url
    alt: "/usr/local/var/run/libvirt/libvirt-sock not found" # alt text
    caption: "/usr/local/var/run/libvirt/libvirt-sock not found" # display caption under cover
    relative: true # when using page bundles set this to true
    hidden: true # only hide on current single page
images:
- 
tags:
- macos
- bug
- kvm
- libvirtd
- howto
type: post
lastmod: 2022-05-24T04:16:18-05:00
draft: true
---
![/usr/local/var/run/libvirt/libvirt-sock not found error](libvirtd-error-2022-05-24-04-03-36.png)

virt-manager installed using homebrew defaults to `/usr/local/var/run/libvirt/libvirt-sock` for the libvirtd socket location on remote hosts. This is not a valid location and the connection fails.

The work around is to use a custom connection string and pass the correct socket location. e.g.

`qemu+ssh://<user name>@<host address>/system?socket=/var/run/libvirt/libvirt-sock`

![Custom connection string for remote libvirtd socket](libvirtd-error-2022-05-24-04-32-00.png)
