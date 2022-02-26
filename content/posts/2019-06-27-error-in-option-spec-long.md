---
title: 'Error in option spec: “long|!”'
author: Danesh Manoharan
date: 2019-06-27T00:09:28+00:00

---
Installed mytop on a CentOS 6.2 box and ran into a bug. 

The fix was simple. Comment out the problem line in the perl file.

```
[root@dbserver local]# mytop
Error in option spec: "long|!"

[root@dbserver local]# which mytop
/usr/bin/mytop

[root@dbserver local]# vi /usr/bin/mytop

From 
     "long|!"              => \$config{long_nums},

To
#     "long|!"              => \$config{long_nums},
```