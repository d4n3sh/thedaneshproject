---
title: 'Linux Tip #6: Download with cURL'
author: Danesh
date: 2009-04-24T01:00:31+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 1903
dsq_thread_id:
  - 889931010

---
Here's how to download a file using cURL.

`curl -O [full url to file]`

`curl -O http://downloads.wordpress.org/plugin/simple-tags.1.6.6.zip`

Sample Output;

`[root@kmon01 bin]# curl -O http://downloads.wordpress.org/plugin/simple-tags.1.6.6.zip<br />
%     Total    % Received % Xferd  Average Speed   Time    Time     Time  Current<br />
                                                      Dload     Upload  Total   Spent    Left   Speed<br />
100  585k    0  585k        0         0 95317             0 --:--:--  0:00:06 --:--:--  120k`