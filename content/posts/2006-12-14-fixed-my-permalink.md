---
title: Fixed my permalink | WordPress
author: Danesh
date: 2006-12-14T12:30:18+00:00
pvc_views:
  - 12126
dsq_thread_id:
  - 889736836

---
Being hosted on godaddy with a basic package ain't the best idea in town. I've been trying to get permalink to work for quite some time now and finally today I managed to get it to work with a few simple entries.  
**Fix;**

1. Modified the php.ini file on my domain root directory  
2. Added the entries below to it

  * cgi.fix_pathinfo = 1
  * cgi.force_redirect = 0

3. Goto WP's Admin -> Options -> Permalinks. Choose you desired option and save.

[<img src="/techblog/wp-content/uploads/2006/12/wp-admin.thumbnail.png" id="image6" alt="WP-Admin page" />][1]{.imagelink}[<img src="/techblog/wp-content/uploads/2006/12/php-ini.thumbnail.png" id="image8" alt="my php.ini file" />][2]{.imagelink}[<img src="/techblog/wp-content/uploads/2006/12/url.thumbnail.png" id="image7" alt="Url reflecting permalink" />][3]{.imagelink}

[[Source]][4]

 [1]: /techblog/wp-content/uploads/2006/12/wp-admin.png "WP-Admin page"
 [2]: /techblog/wp-content/uploads/2006/12/php-ini.png "my php.ini file"
 [3]: /techblog/wp-content/uploads/2006/12/url.png "Url reflecting permalink"
 [4]: http://blog.taragana.com/index.php/archive/wordpress-tip-on-permalink-options/ "http://blog.taragana.com/index.php/archive/wordpress-tip-on-permalink-options/"