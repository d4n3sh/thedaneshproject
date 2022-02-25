---
title: Installing yum fastest mirror plugin on CentOS 5
author: Danesh
date: 2007-05-08T07:02:28+00:00
pvc_views:
  - 7664
dsq_thread_id:
  - 889736367

---
Being in Malaysia don&#8217;t expect the best speeds when running &#8220;**_yum -y update_**&#8220;. I recommend installing the yum fastest mirror plugin to see some better results.

The plugin basically goes through the list of mirrors and determines which mirrors have the best response time. The results are then sorted and stored in a local cached copy.

Installation is simple,

1. # &#8220;_**yum install yum-fastestmirror**_&#8221; for CentOS 5 and &#8220;_**yum -y install yum-plugin-fastestmirror**_&#8221; for previous versions.

2. # &#8220;**_vi /etc/yum/pluginconf.d/fastestmirror.conf_**&#8221; ensure the settings described below and set properly.

>  _[main]  
> enabled=1  
> verbose=0  
> socket_timeout=3  
> hostfilepath=/var/cache/yum/timedhosts.txt  
> maxhostfileage=1_

3. # &#8220;**_yum -y update_**&#8221; and you should start seeing a difference.

> _\# yum -y update  
> Loading &#8220;fastestmirror&#8221; plugin  
> Loading &#8220;installonlyn&#8221; plugin  
> Setting up Update Process  
> Setting up repositories  
> Loading mirror speeds from cached hostfile_

More help available at the [CentOs Wiki][1] .

 [1]: http://wiki.centos.org/PackageManagement/Yum/FastestMirror