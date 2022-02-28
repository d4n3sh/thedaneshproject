---
title: Simple Tags not working with WordPress 2.9
author: Danesh Manoharan
date: 2009-12-27T06:03:46+00:00
pvc_views:
  - 3248
dsq_thread_id:
  - 912005653

---
![](/wp-content/uploads/2009/12/simple-tags-wp2.9-error.png)
Upgraded to WordPress 2.9 and your simple tags plugin stopped working? Here's a quick fix till the [author][1] releases a new version.

`// Check version.<br />
global $wp_version;<br />
if ( strpos($wp_version, '2.7') !== false || strpos($wp_version, '2.8') !== false  ) {<br />
require(dirname(__FILE__).'/2.7/simple-tags.client.php');`

Change it to;

`// Check version.<br />
global $wp_version;<br />
if ( strpos($wp_version, '2.7') !== false || strpos($wp_version, '2.8') !== false || strpos($wp_version, '2.9') !== false  ) {<br />
require(dirname(__FILE__).'/2.7/simple-tags.client.php');`

Basically add "|| strpos($wp_version, '2.9') !== false" at the end of the if statement.

 [1]: http://wordpress.org/extend/plugins/simple-tags/