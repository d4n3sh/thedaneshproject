---
title: How to find files in linux
author: Danesh
date: 2008-01-15T20:23:25+00:00
url: /posts/how-to-find-files-in-linux/
pvc_views:
  - 12233
dsq_thread_id:
  - 896237097

---
Need to find files older than certain time frame? This will help, &#8220;find [dir] -type f -mtime +[24hours*n] &#8221;

Examples,

Show files older than 7 days

    find /tmp/ -type f -mtime +7

Show files older than 7 days and rm them.

    find /tmp/ -type f -mtime +7 -exec rm {} \;

or if you have a large number of files

    find /tmp/ -type f -mtime +7 | xargs rm