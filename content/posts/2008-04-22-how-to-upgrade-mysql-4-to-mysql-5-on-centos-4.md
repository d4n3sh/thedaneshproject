---
title: How to upgrade MySQL 4 to MySQL 5 on CentOS 4
author: Danesh
date: 2008-04-22T07:29:04+00:00
pvc_views:
  - 7971
dsq_thread_id:
  - 890811737

---
I was playing a round with new software today which needed MySQL 5. My server's running CentOS 4.6 which ships by default with MySQL 4.

The to upgrade to MySQL 5 from MySQL 4 is easy. There are 2 options you could use.

The first option would require you to remove all MySQL 4 packages by running,

`># yum remove mysql`

The seconf option is way simpler.

`># yum --enablerepo=centosplus update mysql`

This will download MySQL 5 from the plus repository and replace the installed MySQL 4.

Remeber to backup your DBs before updating.