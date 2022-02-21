---
title: How to set the date and time in Archlinux
author: Danesh
date: 2013-01-20T17:04:58+00:00
pvc_views:
  - 180
dsq_thread_id:
  - 1036843055

---
Quickly set the current date and time in Archlinux. 

1. Check the current time.  
`[root@atom ~]# timedatectl status<br />
      Local time: Mon 2013-01-21 08:57:21 MYT<br />
  Universal time: Mon 2013-01-21 00:57:21 UTC<br />
        RTC time: Mon 2013-01-21 00:57:21<br />
        Timezone: Asia/Kuala_Lumpur (MYT, +0800)<br />
     NTP enabled: no<br />
NTP synchronized: no<br />
 RTC in local TZ: no<br />
      DST active: n/a`

2. Set the correct date and time.  
`[root@atom ~]# timedatectl set-time "2013-01-21 00:59:00"`

3. Check again, make sure the date and time looks right now.  
`[root@atom ~]# timedatectl status<br />
      Local time: Mon 2013-01-21 00:59:14 MYT<br />
  Universal time: Sun 2013-01-20 16:59:14 UTC<br />
        RTC time: Sun 2013-01-20 16:59:14<br />
        Timezone: Asia/Kuala_Lumpur (MYT, +0800)<br />
     NTP enabled: no<br />
NTP synchronized: no<br />
 RTC in local TZ: no<br />
      DST active: n/a<br />
`