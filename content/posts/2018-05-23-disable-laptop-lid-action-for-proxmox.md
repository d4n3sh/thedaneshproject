---
title: Disable laptop lid action for proxmox
author: Danesh Manoharan
date: 2018-05-22T22:13:31+00:00

---
I run a low power proxmox server using my old Lenovo T430s. It's headless so the lid's always closed.

When I first set it up, closing the lid would send the laptop into standby mode. Here's what I did to get promox/debian to ignore the laptop lid action.

Edit the /etc/systemd/logind.conf file

Change the lines below.

```
HandleLidSwitch=ignore
HandleLidSwitchDocked=ignore
```

restart the logind service.

```
#systemctl restart systemd-logind.service
```

 