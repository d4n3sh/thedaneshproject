---
title: What does dirname(__FILE__) and basename(dirname(__FILE__)) do?
author: Danesh
date: 2009-02-06T09:44:06+00:00
url: /posts/what-does-dirname__file__-and-basenamedirname__file__-do/
pvc_views:
  - 32501
robotsmeta:
  - index,follow
dsq_thread_id:
  - 889774814

---
Was helping a friend fix his php script today. He was not too sure about what &#8220;dirname(\_\_FILE\_\_)&#8221; did.

dirname() is a PHP function which returns the directory name of a file. For example if file abc.txt was in &#8220;/tmp/abc.txt&#8221; then the dirname() function would return &#8220;/tmp&#8221; .

Example Usage;

`<?php`

$file = &#8220;/tmp/abc.txt&#8221;;

$path = dirname($file); // $path will now contain /tmp

?>

What does dirname(\_\_FILE\_\_) and basename(dirname(\_\_FILE\_\_)) do then?

The \_\_FILE\_\_ constantÂ  represents the running script. It will return the full path and file name of the running script. For example, theÂ  \_\_FILE\_\_ constantÂ  on my server would return &#8220;/var/www/html/index.php&#8221; for my index.php file which is in the &#8220;/var/www/html/&#8221; directory.

The basename() command is normally used in conjunction with the dirname() function to strip the parent directory from a full file name. For example &#8220;/var/www/html/abc.txt&#8221; when passed through basename() would return abc.txt. basename() also works on directories. So, basename() on &#8220;/var/www/html&#8221; would return &#8220;html&#8221; since in Linux directories are files.

Example Usage;

Imagine \_\_FILE\_\_ represents /var/www/html/index.php

`<?php`

echo dirname(\_\_FILE\_\_); // returns /var/www/html

echo basename(\_\_FILE\_\_); //returns index.php

echo basename(dirname(\_\_FILE\_\_)); //returns html

?>