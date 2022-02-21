---
title: How to install mscore fonts on openSUSE 11.0
author: Danesh
date: 2008-06-22T07:11:05+00:00
pvc_views:
  - 7128
dsq_thread_id:
  - 891200181

---
Install the cabextract package.

`abooboo># zypper in cabextract`

Download the msfont installer script for openSUSE 10.3.

`abooboo># wget http://download.opensuse.org/update/10.3/scripts/fetchmsttfonts.sh`

Assign execute permission and execute the script.

`abooboo># chmod a+x fetchmsttfonts.sh</p>
<p>abooboo># ./fetchmsttfonts.sh`

You have ms fonts now. The other simpler way to do this is to simply copy over the fonts you need from a Windows machine and use the fonts manager to install them.