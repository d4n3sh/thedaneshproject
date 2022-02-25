---
title: How to find recently installed RPMs
author: Danesh
date: 2008-05-05T03:03:38+00:00
pvc_views:
  - 9710
dsq_thread_id:
  - 889977436

---
`rpm -qa --last` will return all installed rpm packages with their installed time. The last installed packages will be at the top of the list.

`rpm -qa --last | less` is will return all installed packages with their install date. Less allows you to scroll through the results. 

`rpm -qa --last | tail -n [lines]` will return the last 5 packages. Replace [line] with any number you want, in my case 5 for file lines.

`[root@bambee root]# rpm -qa --last | tail -n 5<br />
termcap-11.0.1-17.1                           Tue 09 May 2006 03:02:53 PM MYT<br />
setup-2.5.27-1                                Tue 09 May 2006 03:02:52 PM MYT<br />
filesystem-2.2.1-3                            Tue 09 May 2006 03:02:52 PM MYT<br />
basesystem-8.0-2                              Tue 09 May 2006 03:02:52 PM MYT<br />
redhat-logos-1.1.14.3-1                       Tue 09 May 2006 03:02:51 PM MYT`

`rpm -qa --last | grep [package name]` will return the install date for a specific RPM package. In my case the apache web server [httpd]

`[root@jumbo root]# rpm -qa --last | grep httpd<br />
redhat-config-httpd-1.1.0-4.30.2              Sat 29 Mar 2008 09:03:40 PM MYT<br />
httpd-2.0.46-70.ent                           Sat 29 Mar 2008 08:58:19 PM MYT`