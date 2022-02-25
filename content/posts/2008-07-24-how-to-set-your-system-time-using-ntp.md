---
title: How to set your system time using NTP
author: Danesh
date: 2008-07-24T08:13:27+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 6868
dsq_thread_id:
  - 890109013

---
Here's a quick walk through to synchronize your system time through NTP.

Install the NTP package if you don't already have it installed.

`[root@abubu]# yum install ntp`

Check your date.

`[root@abubu]# date<br />
Thu Jul 24 13:34:24 MYT 2008`

Use the ntpdate command to poll from public NTP servers. I this example I'll use ntp servers provided by the [NTP POOL Project][1]. The asia pool is &#8220;ntp asia.pool.ntp.org&#8221;

<figure style="width: 125px" class="wp-caption alignnone">[<img loading="lazy" title="NTP POOL PROJECT" src="http://st.ntppool.net/images/logo.v1.png" alt="NTP POOL PROJECT" width="125" height="138" />][2]<figcaption class="wp-caption-text">NTP POOL PROJECT</figcaption></figure>

`[root@abubu]# ntpdate asia.pool.ntp.org<br />
24 Jul 16:02:18 ntpdate[5316]: step time server 202.144.207.222 offset -28647.175440 sec`

Check your time again to make sure it's correct.

`[root@abubu]# date<br />
Thu Jul 24 16:02:24 MYT 2008`

I'll cover the ntpd daemon in a future post.

 [1]: http://www.pool.ntp.org/zone/asia
 [2]: http://www.pool.ntp.org