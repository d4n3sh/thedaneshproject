---
title: Installing yum fastest mirror plugin on CentOS 5
author: Danesh Manoharan
date: 2007-05-08T07:02:28+00:00
pvc_views:
  - 7664
dsq_thread_id:
  - 889736367

---
Being in Malaysia don't expect the best speeds when running "**_yum -y update_**". I recommend installing the yum fastest mirror plugin to see some better results.

The plugin basically goes through the list of mirrors and determines which mirrors have the best response time. The results are then sorted and stored in a local cached copy.

Installation is simple,

1. # "_**yum install yum-fastestmirror**_" for CentOS 5 and "_**yum -y install yum-plugin-fastestmirror**_" for previous versions.

2. # "**_vi /etc/yum/pluginconf.d/fastestmirror.conf_**" ensure the settings described below and set properly.

>  _[main]  
> enabled=1  
> verbose=0  
> socket_timeout=3  
> hostfilepath=/var/cache/yum/timedhosts.txt  
> maxhostfileage=1_

3. # "**_yum -y update_**" and you should start seeing a difference.

> _\# yum -y update  
> Loading "fastestmirror" plugin  
> Loading "installonlyn" plugin  
> Setting up Update Process  
> Setting up repositories  
> Loading mirror speeds from cached hostfile_

More help available at the [CentOs Wiki][1] .

 [1]: http://wiki.centos.org/PackageManagement/Yum/FastestMirror