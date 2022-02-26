---
title: Extract .xz file
author: Danesh Manoharan
date: 2019-06-10T22:20:49+00:00

---
I generally just use the tar utility to extract files from a [.xz][1] archive.


```
>_ file tsetup.1.7.7.tar.xz
  tsetup.1.7.7.tar.xz: XZ compressed data

  
>_ tar -tvf tsetup.1.7.7.tar.xz
  drwxrwxr-x preston/preston   0 2019-06-10 05:25 Telegram/
  -rwxrwxr-x preston/preston 97436648 2019-06-10 05:24 Telegram/Telegram
  -rwxrwxr-x preston/preston  1400643 2019-06-10 04:52 Telegram/Updater

  >_ tar -xvf tsetup.1.7.7.tar.xz
  Telegram/
  Telegram/Telegram
  Telegram/Updater

  
>_ ls -l Telegram/
  total 96524
  -rwxrwxr-x. 1 user1 user1 97436648 Jun 10 05:24 Telegram
  -rwxrwxr-x. 1 user1 user1  1400643 Jun 10 04:52 Updater
```

 [1]: https://en.wikipedia.org/wiki/Xz
