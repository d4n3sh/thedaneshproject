---
title: Installing RHEL EPEL Repo on CentOS 5.x
author: Danesh
date: 2013-08-27T08:15:23+00:00
dsq_thread_id:
  - 1653411171

---
Had to get collectd going on a CentOS 5.8 environment today. The EPEL repo was needed to get the packages.

Here&#8217;s how to add the EPEL repo to CentOS 5.x

`cd /tmp`  
`wget http://dl.fedoraproject.org/pub/epel/5/x86_64/epel-release-5-4.noarch.rpm`

`rpm -Uvh epel-release-5-4.noarch.rpm`