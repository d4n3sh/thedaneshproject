---
title: Firefox slow on Ubuntu 10.04
author: Danesh
date: 2010-05-06T03:36:05+00:00
url: /posts/firefox-slow-on-ubuntu-10-04/
pvc_views:
  - 2814
dsq_thread_id:
  - 891895942

---
If your Firefox is sluggish on on Ubuntu 10.04 this might help.

Fire up Firefox and type &#8220;about:config&#8221; in the URL bar. That will bring up the config page.

Search for the lines below and change them accordingly to reflect the changes below.

`- network.http.pipelining > Make it True<br />
- network.http.pipelining.maxrequests > Make it 8 or 10<br />
- network.http.proxy.pipelining > Make it True<br />
- network.dns.disableIPv6 > Make it True`