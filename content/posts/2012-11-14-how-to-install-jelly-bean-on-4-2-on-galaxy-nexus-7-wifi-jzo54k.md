---
title: How To Install Jelly Bean on 4.2 on Galaxy Nexus 7 WiFi JZO54K
author: Danesh Manoharan
date: 2012-11-14T08:22:21+00:00
pvc_views:
  - 1349
dsq_thread_id:
  - 927354388

---
<a href="/posts/how-to-install-jelly-bean-on-4-2-on-galaxy-nexus-7-wifi-jzo54k/jb-new-logo/" rel="attachment wp-att-3081"><img loading="lazy" class="alignnone size-full wp-image-3081" title="jb-new-logo" src="/wp-content/uploads/2012/11/jb-new-logo.png" alt="" width="206" height="316" /></a>

Google has released the official Jelly Bean 4.2 images to its servers. If you can't wait for the OTA like me then the manual method will get you 4.2 now. See how below,

I'm doing this on Fedora 17

**<span style="color: #ff0000;">NOTICE: Do this at your own risk. There is a chance of things going wrong and you might end up with a brick.</span>**

1. install adb and fastboot  
`yum install android-tools`  
2. Download the Jelly Bean 4.2 (JOP40C) factory image. [Link][1]  
`wget https://dl.google.com/dl/android/aosp/nakasi-jop40c-factory-6aabb391.tgz`  
3. Extract the downloaded file.  
`tar -zxvf nakasi-jop40c-factory-6aabb391.tgz<br />
cd nakasi-jop40c/`  
4. Make the install scripts executable.  
`chmod +x flash-all.sh<br />
chmod +x flash-base.sh`  
flash-all.sh will erase all data and flash everything.  
flash-base.sh will only flash the bootloader and radio.

5. Make user USB debugging is on for your Nexus 7.

Settings -> Developer Options -> "On" -> USB Debugging -> "On"

6. Boot into fastboot

power off -> power on (hold power + volume down)till you get into the fastboot screen.

7. Unlock the boot loader.  
`fastboot oem unlock`  
confirm on your Nexus 7 screen.

8. Run the install script.  
`./flash-all.sh`

 [1]: https://dl.google.com/dl/android/aosp/nakasi-jop40c-factory-6aabb391.tgz