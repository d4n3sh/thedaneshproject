---
title: 'Error in option spec: “long|!”'
author: Danesh
date: 2019-06-27T00:09:28+00:00

---
Installed mytop on a CentOS 6.2 box and ran into a bug. 

The fix was simple. Comment out the problem line in the perl file.

<pre class="wp-block-code"><code>&#91;root@dbserver local]# mytop
Error in option spec: "long|!"

&#91;root@dbserver local]# which mytop
/usr/bin/mytop

&#91;root@dbserver local]# vi /usr/bin/mytop

From 
     "long|!"              => \$config{long_nums},

To
#     "long|!"              => \$config{long_nums},</code></pre>