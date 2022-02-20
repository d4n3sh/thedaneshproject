---
title: How to disable selinux in CentOS 5.2
author: Danesh
date: 2008-12-16T15:24:11+00:00
url: /posts/how-to-disable-selinux-in-centos-52/
robotsmeta:
  - index,follow
pvc_views:
  - 11160
dsq_thread_id:
  - 889760653

---
Here&#8217;s how you would disable SELinux permanently.

1. vi the &#8220;**/etc/selinux/config**&#8221; file.

2. Change the following line;

`SELINUX=enforcing` to `SELINUX=disabled`

3.Â  Save the file and reboot.

4. To verify if SELinux is disabled, run &#8220;`dmesg | grep selinux`&#8220;. You should see `selinux=0`

selinux\_register\_security:Â  Registering secondary module capability  
audit(1229470429.628:2): selinux=0 auid=4294967295 ses=4294967295

My /etc/selinux/config file.  
`<br />
# This file controls the state of SELinux on the system.<br />
# SELINUX= can take one of these three values:<br />
#Â Â Â Â Â Â  enforcing - SELinux security policy is enforced.<br />
#Â Â Â Â Â Â  permissive - SELinux prints warnings instead of enforcing.<br />
#Â Â Â Â Â Â  disabled - SELinux is fully disabled.<br />
#SELINUX=enforcing<br />
SELINUX=disabled<br />
# SELINUXTYPE= type of policy in use. Possible values are:<br />
#Â Â Â Â Â Â  targeted - Only targeted network daemons are protected.<br />
#Â Â Â Â Â Â  strict - Full SELinux protection.<br />
SELINUXTYPE=targeted`