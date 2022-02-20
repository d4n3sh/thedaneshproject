---
title: 'Firefox tweak: Use Ram as Cache'
author: Danesh
date: 2010-12-05T05:52:00+00:00
url: /posts/firefox-tweak-use-ram-as-cache/
pvc_views:
  - 3188
dsq_thread_id:
  - 896027720

---
By design Firefox will use your disk as cache. However, if you have a good amount of RAM available you could quickly improve Firefox&#8217;s performance by telling it disable disk caching and only use RAM.

Here&#8217;s how you do it;

1. in your URL bar type in &#8220;about:config&#8221;. this will bring up the config page.

2. Using the filter box, lookup &#8220;browser.cache.disk.enable&#8221;. Change its value to &#8220;False&#8221; by double clicking on it.

3. Using the filter box again, lookup &#8220;browser.cache.memory.enable&#8221; . Change its value to &#8220;True&#8221; by double clicking on it.

`browser.cache.disk.enable to False<br />
browser.cache.memory.enable to True`