---
title: What does dirname(__FILE__) and basename(dirname(__FILE__)) do?
author: Danesh Manoharan
date: 2009-02-06T09:44:06+00:00
pvc_views:
  - 32501
robotsmeta:
  - index,follow
dsq_thread_id:
  - 889774814

---
Was helping a friend fix his php script today. He was not too sure about what "dirname(\_\_FILE\_\_)" did.

dirname() is a PHP function which returns the directory name of a file. For example if file abc.txt was in "/tmp/abc.txt" then the dirname() function would return "/tmp" .

Example Usage;

`<?php`

$file = "/tmp/abc.txt";

$path = dirname($file); // $path will now contain /tmp

?>

What does dirname(\_\_FILE\_\_) and basename(dirname(\_\_FILE\_\_)) do then?

The \_\_FILE\_\_ constantÂ  represents the running script. It will return the full path and file name of the running script. For example, theÂ  \_\_FILE\_\_ constantÂ  on my server would return "/var/www/html/index.php" for my index.php file which is in the "/var/www/html/" directory.

The basename() command is normally used in conjunction with the dirname() function to strip the parent directory from a full file name. For example "/var/www/html/abc.txt" when passed through basename() would return abc.txt. basename() also works on directories. So, basename() on "/var/www/html" would return "html" since in Linux directories are files.

Example Usage;

Imagine \_\_FILE\_\_ represents /var/www/html/index.php

`<?php`

echo dirname(\_\_FILE\_\_); // returns /var/www/html

echo basename(\_\_FILE\_\_); //returns index.php

echo basename(dirname(\_\_FILE\_\_)); //returns html

?>