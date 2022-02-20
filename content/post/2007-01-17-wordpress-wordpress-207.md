---
title: WordPress 2.0.7 Released | WordPress
author: Danesh
date: 2007-01-17T11:33:10+00:00
url: /posts/wordpress-wordpress-207/
pvc_views:
  - 2127
dsq_thread_id:
  - 915200329

---
<img src="/techblog/wp-content/uploads/2007/01/wp-20-square-button.gif" alt="wp-20-square-button.gif" id="image50" />WordPress 2.0.7 has been realease to address a few security issue that showed up in 2.0.6. Everyone running 2.0.6 or lower are adviced to get this upgrade ASAP.

**Change Log**

  * Security fix for `wp_unregister_GLOBALS()` to work around the <a href="http://www.hardened-php.net/hphp/zend_hash_del_key_or_index_vulnerability.html" target="_blank">zend_hash_del_key_or_index bug</a> in PHP 4 versions less than 4.4.3 and PHP 5 versions less than 5.1.4 with `register_globals` set to â€œOn.â€
  * Feeds now properly serve `304 Not Modified` headers instead of mismatched 200/304 headers (a.k.a. the FeedBurner bug).
  * Backport of another `304 Not Modified` fix from WordPress 2.1
  * Deleting WordPress Pages no longer gives an â€œAre You Sure?â€ prompt.
  * After deleting a WordPress Page, you are now properly redirected to the Edit Pages screen.
  * Sending an image at original size in Internet Explorer no longer adds an incorrect â€œheightâ€ attribute.

[Development Blog â€º WordPress 2.0.7][1]

 [1]: http://wordpress.org/development/2007/01/wordpress-207/