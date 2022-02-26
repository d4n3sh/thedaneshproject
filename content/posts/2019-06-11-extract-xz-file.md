---
title: Extract .xz file
author: Danesh Manoharan
date: 2019-06-10T22:20:49+00:00

---
I generally just use the tar utility to extract files from a [.xz][1] archive.



<pre class="wp-block-preformatted">>_ file tsetup.1.7.7.tar.xz<br />  tsetup.1.7.7.tar.xz: XZ compressed data<br /><br />  >_ tar -tvf tsetup.1.7.7.tar.xz<br />  drwxrwxr-x preston/preston   0 2019-06-10 05:25 Telegram/<br />  -rwxrwxr-x preston/preston 97436648 2019-06-10 05:24 Telegram/Telegram<br />  -rwxrwxr-x preston/preston  1400643 2019-06-10 04:52 Telegram/Updater<br /><br />  >_ tar -xvf tsetup.1.7.7.tar.xz<br />  Telegram/<br />  Telegram/Telegram<br />  Telegram/Updater<br /><br />  >_ ls -l Telegram/<br />  total 96524<br />  -rwxrwxr-x. 1 user1 user1 97436648 Jun 10 05:24 Telegram<br />  -rwxrwxr-x. 1 user1 user1  1400643 Jun 10 04:52 Updater</pre>

 [1]: https://en.wikipedia.org/wiki/Xz