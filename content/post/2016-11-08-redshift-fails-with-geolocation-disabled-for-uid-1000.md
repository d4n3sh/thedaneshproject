---
title: redshift fails with Geolocation disabled for UID 1000
author: Danesh
date: 2016-11-08T15:15:52+00:00
url: /posts/redshift-fails-with-geolocation-disabled-for-uid-1000/
dsq_thread_id:
  - 5288533538

---
Installed redshift on my Arch box today but it kept failing with &#8220;Geolocation disabled for UID 1000&#8221;. This is a bug which will be fixed in a new release but till then here&#8217;s an easy work around.

Add the lines below to the /etc/geoclue/geoclue.conf file and restart gnome.

<pre class="">[redshift]
allowed=true
system=false
users=</pre>

&nbsp;