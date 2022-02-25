---
title: How to install Flash 11 64-bit on Fedora 16
author: Danesh Manoharan
date: 2011-11-09T12:54:04+00:00
pvc_views:
  - 10027
dsq_thread_id:
  - 889891512

---
Change into you home directory.  
`cd ~`  
Download the official Adobe repository package rpm. This rpm will create the repository file for us.  
`sudo wget http://linuxdownload.adobe.com/linux/x86_64/adobe-release-x86_64-1.0-1.noarch.rpm`  
Install the rpm file.  
`sudo rpm -ivh adobe-release-x86_64-1.0-1.noarch.rpm`  
Import the repository GPG key.  
`sudo rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-adobe-linux`  
Update you local yum repositories.  
`sudo yum update`  
Install the 64 bit Flash Plugin  
`sudo yum -y install flash-plugin`

Check if the install was successful. In Firefox, go to "about:plugins" in the address bar and look for "Shockwave Flash". If installed you will see;

    `File: libflashplayer.so<br />
    Version: Shockwave Flash 11.0 r1`

Quick Step: If you just want to install the Flash Plugin and not bother about the repo you can download the installer directly and install Flash.

`cd ~<br />
sudo wget http://fpdownload.macromedia.com/get/flashplayer/pdc/11.0.1.152/flash-plugin-11.0.1.152-release.x86_64.rpm<br />
sudo rpm -ivh flash-plugin-11.0.1.152-release.x86_64.rpm`