---
title: How to install hddtemp on CentOS 6.2
author: Danesh
date: 2012-02-14T07:04:45+00:00
pvc_views:
  - 1984
dsq_thread_id:
  - 890442295

---
[hddtemp][1] is a simple small app to monitor your hard disk temperature. It works by accessing the SMART capability of modern disks.

Here&#8217;s how to install it.

Download and compile from source.  
`#cd /tmp<br />
#wget http://download.savannah.gnu.org/releases/hddtemp/hddtemp-0.3-beta15.tar.bz2<br />
#tar -jxvf hddtemp-0.3-beta15.tar.bz2<br />
#cd hddtemp-0.3-beta15<br />
#./configure<br />
#make<br />
#make install<br />
#cd /usr/share/misc/<br />
#wget http://download.savannah.gnu.org/releases/hddtemp/hddtemp.db`

Test it.  
`#hddtemp /dev/sda<br />
#/dev/sda: WDC WD2500JS-75NCB3   : 45°C`

 [1]: https://savannah.nongnu.org/projects/hddtemp/