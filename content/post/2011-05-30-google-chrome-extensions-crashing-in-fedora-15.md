---
title: Google Chrome extensions crashing in Fedora 15
author: Danesh
date: 2011-05-30T03:43:53+00:00
url: /posts/google-chrome-extensions-crashing-in-fedora-15/
pvc_views:
  - 5917
dsq_thread_id:
  - 899000758

---
<img loading="lazy" class="alignnone size-medium wp-image-2271" title="chrome-error-f15" src="/wp-content/uploads/2011/05/chrome-error-f15-450x106.png" alt="" width="450" height="106" srcset="/wp-content/uploads/2011/05/chrome-error-f15-450x106.png 450w, /wp-content/uploads/2011/05/chrome-error-f15.png 767w" sizes="(max-width: 450px) 100vw, 450px" />

Many have been complaining of their chrome extensions crashing in Fedora 15. In my case it was LastPass and Xmarks.

The issue is caused by SELinux and the quick fix is to disable SELinux. Here&#8217;s how you get it done;

1. Fire up a terminal

2. cd to /etc/selinux/

3. vi the &#8220;config&#8221; file.

4. Change &#8220;SELINUX=enforcing&#8221; to &#8220;SELINUX=disabled&#8221;

5. Reboot, launch Chrome and your extensions should be working fine.