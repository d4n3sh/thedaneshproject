---
title: How to Fix Ubuntu 10.10 VirtualBox Guest Additions Problems
author: Danesh Manoharan
date: 2010-09-27T14:08:07+00:00
pvc_views:
  - 13015
dsq_thread_id:
  - 890794478

---
If you're trying to run Ubuntu 10.10 Beta on your VirtualBox, you're most likely having issues with the screen resolution. Installing the default VirtualBox client doesn't quite help. Try the steps below,

1. Open terminal and enter the following command:

`#sudo apt-get update<br />
#sudo apt-get install build-essential linux-headers-$(uname -r)<br />
#sudo apt-get install virtualbox-ose-guest-x11`

2. Once installation is finished, restart your VirtualBox machine.

3. Go to System ->Preferences ->Monitors and change the resolution of your screen. You might be able to change the resolution but the screen will re-size properly when you maximize.