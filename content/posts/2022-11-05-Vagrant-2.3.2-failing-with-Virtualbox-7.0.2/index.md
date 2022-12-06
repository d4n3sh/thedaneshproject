---
author: "Danesh Manoharan"
title: "Vagrant 2.3.2 Failing With Virtualbox 7.0.2"
date: 2022-11-05T23:32:22+08:00
description: "Vagrant can't create a host-only private network on Virtualbox 7, use intnet instead." # Post description, shows up below title
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: true # when using page bundles set this to true
    hidden: true # only hide on current single page
images:
- 
tags:
- virtualbox
- vagrant
- macos
- ventura
lastmod: 2022-11-05T23:32:22+08:00
draft: false
---
```shell
There was an error while executing `VBoxManage`, a CLI used by Vagrant
for controlling VirtualBox. The command and stderr is shown below.

Command: ["hostonlyif", "create"]

Stderr: 0%...NS_ERROR_FAILURE
VBoxManage: error: Failed to create the host-only adapter
VBoxManage: error: VBoxNetAdpCtl: Error while adding new interface: failed to open /dev/vboxnetctl: No such file or directory
VBoxManage: error: Details: code NS_ERROR_FAILURE (0x80004005), component HostNetworkInterfaceWrap, interface IHostNetworkInterface
VBoxManage: error: Context: "RTEXITCODE handleCreate(HandlerArg *)" at line 105 of file VBoxManageHostonly.cpp
```

Vagrant currently can't create host-only networks on Virtualbox 7. [Github issue 12967](https://github.com/hashicorp/vagrant/issues/12967)

The workaround, for now, is to use Virtualbox's "internal network" private network. I've tested this as it works on macOS Ventura.

```bash
  config.vm.define "host1" do |host1|
      host1.vm.hostname = "n2"
      host1.vm.network "private_network", ip: "192.168.56.11",
        virtualbox__intnet: true
  end
```

