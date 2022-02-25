---
title: Disable IPv6 in Firefox 3
author: Danesh
date: 2010-01-10T18:33:44+00:00
pvc_views:
  - 20902
dsq_thread_id:
  - 889880567

---
Firefox 3 by default resolves IPv6 address first and if that fails then reverts to IPv4. This can sometimes slow down your browser&#8217;s performance.

Here are the steps to turn off IPv6 support in Firefox 3 and above.

1. Key in &#8220;about:config&#8221; into address bar, this will take you to the config page.

2. Key in &#8220;network.dns.disableIPv6&#8221;  into the filter bar and hit enter.

<img loading="lazy" class="alignnone size-medium wp-image-1945" title="snapshot1" src="/wp-content/uploads/2010/01/snapshot1-450x115.png" alt="" width="450" height="115" srcset="/wp-content/uploads/2010/01/snapshot1-450x115.png 450w, /wp-content/uploads/2010/01/snapshot1-1024x262.png 1024w, /wp-content/uploads/2010/01/snapshot1.png 1070w" sizes="(max-width: 450px) 100vw, 450px" /> 

3. Right click on the line that read &#8220;network.dns.disableIPv6&#8221; and select the &#8220;Toggle&#8221; option. This will switch the value from &#8220;false&#8221; to &#8220;true&#8221;

<img loading="lazy" class="alignnone size-medium wp-image-1945" title="snapshot1" src="/wp-content/uploads/2010/01/snapshot1-450x115.png" alt="" width="450" height="115" srcset="/wp-content/uploads/2010/01/snapshot1-450x115.png 450w, /wp-content/uploads/2010/01/snapshot1-1024x262.png 1024w, /wp-content/uploads/2010/01/snapshot1.png 1070w" sizes="(max-width: 450px) 100vw, 450px" /> 

4. Restart the browser and enjoy the improvement.