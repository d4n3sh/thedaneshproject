---
title: 'Firefox tweak: Use Ram as Cache'
author: Danesh
date: 2010-12-05T05:52:00+00:00
pvc_views:
  - 3188
dsq_thread_id:
  - 896027720

---
By design Firefox will use your disk as cache. However, if you have a good amount of RAM available you could quickly improve Firefox's performance by telling it disable disk caching and only use RAM.

Here's how you do it;

1. in your URL bar type in "about:config". this will bring up the config page.

2. Using the filter box, lookup "browser.cache.disk.enable". Change its value to "False" by double clicking on it.

3. Using the filter box again, lookup "browser.cache.memory.enable" . Change its value to "True" by double clicking on it.

`browser.cache.disk.enable to False<br />
browser.cache.memory.enable to True`