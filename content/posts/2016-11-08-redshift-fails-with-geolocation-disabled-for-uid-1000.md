---
title: redshift fails with Geolocation disabled for UID 1000
author: Danesh
date: 2016-11-08T15:15:52+00:00
dsq_thread_id:
  - 5288533538

---
Installed redshift on my Arch box today but it kept failing with "Geolocation disabled for UID 1000". This is a bug which will be fixed in a new release but till then here's an easy work around.

Add the lines below to the /etc/geoclue/geoclue.conf file and restart gnome.

<pre class="">[redshift]
allowed=true
system=false
users=</pre>

 