---
title: How to install webmin on CentOS 4
author: Danesh Manoharan
date: 2008-02-14T13:51:00+00:00
pvc_views:
  - 37950
dsq_thread_id:
  - 890033273

---
Webmin is a web based control panel for system administrators for Unix/Linux. I use Webmin for reports mainly. More about Webmin [here][1].

This is how you would install Webmin on Centos 4.

1. First start by downloading the latest version of [Webmin][2]. The current version is 1.400.

I prefer to use use wget to directly download the file onto the server but it's up to you.

```
wget http://prdownloads.sourceforge.net/webadmin/webmin-1.400-1.noarch.rpm
```

2. Install the Webmin rpm package.

```
rpm -ivh  webmin-1.400-1.noarch.rpm
```

```
[root@proxy0 /]# rpm -ivh webmin-1.400-1.noarch.rpm
warning: webmin-1.400-1.noarch.rpm: V3 DSA signature: NOKEY, key ID 11f63c51
Preparing...                ########################################### [100%]
Operating system is CentOS Linux
1:webmin                 ########################################### [100%]
Webmin install complete. You can now login to https://proxy0.klm1.netcel360.com:10000/
as root with your root password.
```

3. Check if the Webmin service has been started.

```
service webmin status
```

```
[root@proxy0 /]# service webmin status
webmin (pid 4878) is running
```

That's it, you can now login using your _**root**_ id at https://localhost:10000

<!--more-->

![](http://img89.imageshack.us/img89/4585/webmin1sgb5.png)

 [1]: http://www.webmin.com/index.html
 [2]: http://www.webmin.com/download.html
 [3]: http://img89.imageshack.us/img89/9980/webmin1bb9.png)