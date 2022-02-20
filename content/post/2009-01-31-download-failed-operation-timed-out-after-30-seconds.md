---
title: 'Download failed.: Operation timed out after 30 seconds'
author: Danesh
date: 2009-01-31T17:33:38+00:00
url: /posts/download-failed-operation-timed-out-after-30-seconds/
robotsmeta:
  - index,follow
pvc_views:
  - 19857
dsq_thread_id:
  - 890951761

---
Been getting this error &#8220;Download failed.: Operation timed out after 30 seconds&#8221; every time I try to update a plug-in in my WordPress 2.7.

After some digging around I found that my web server&#8217;s download speed was pretty low. WP 2.7 by default has a 30 second timeout set for it&#8217;s download function which I constantly kept hitting.

The workaround&#8217;s a simple hack to the file.php file in the /wp-admin/includes/ folder.

1. Download the file using over ftp or ssh. Depending on your hosting package.

2. Look for the line;

&#8221; $response = wp\_remote\_get($url, array(&#8216;timeout&#8217; => 30)); &#8221;

and replace it with;

&#8221; $response = wp\_remote\_get($url, array(&#8216;timeout&#8217; => 60)); &#8221;

function download_url() at wp-admin/includes/file.php

3. Upload the modified file back into the /wp-admin/includes/ folder. Overwrite the old file if you must.

You auto update should be working fine now.