---
title: Install Google Chrome on Fedora 12
author: Danesh
date: 2010-04-17T07:37:49+00:00
pvc_views:
  - 7487
dsq_thread_id:
  - 890112432

---
1. create the repo file. "vi /etc/yum.repos.d/google.repo" and add the following lines into the file.  
`[google]<br />
name=Google - i386<br />
baseurl=http://dl.google.com/linux/rpm/stable/i386<br />
enabled=1<br />
gpgcheck=1<br />
gpgkey=https://dl-ssl.google.com/linux/linux_signing_key.pub<br />
[google-chrome]<br />
name=google-chrome<br />
baseurl=http://dl.google.com/linux/rpm/stable/i386<br />
enabled=1<br />
gpgcheck=1<br />
` 

2. Do a "yum list google-chrome-*" to check if the google-chrome is available for install.  
`[root@dexter ~]# yum list google-chrome-*<br />
..........<br />
.......<br />
google-chrome-beta.i386                                                            5.0.342.9-43360                                                        google<br />
google-chrome-unstable.i386                                                        5.0.375.9-44625                                                        google`

3. Install Google Chrome. "yum install google-chrome-beta"  
`[root@dexter ~]# yum install google-chrome-beta.i386<br />
Running Transaction<br />
  Installing     : google-chrome-beta-5.0.342.9-43360.i386                                                                                                  1/1<br />
.......................<br />
Installed:<br />
  google-chrome-beta.i386 0:5.0.342.9-43360                                                                                                                     ..........................<br />
Complete!`

That's it, enjoy your Chrome 😀