---
title: Ubuntu 11.04 blank screen on boot. SOLVED
author: Danesh Manoharan
date: 2011-05-25T06:40:15+00:00
pvc_views:
  - 90238
dsq_thread_id:
  - 889773817

---
Try these steps if you are experiencing a blank screen during boot or install of Ubuntu 11.04 Natty Narwhal.

1. LiveCD  boots into a blank screen.

When you see the boot menu when you boot LiveCD, hit F6 and select the "nomodeset" option.

2. Boots into a blank screen after install.

Reboot and keep your finger on the "SHIFT" key till you get the grub menu. Highlight the first entry and replace "quiet splash" with "nomodeset" .  Hit CTRL + X to continue booting. Once logged in install the latest Graphics drivers. _System -> Administration -> Additional Drivers_

_DONE. Hope it works for you, it did for me._