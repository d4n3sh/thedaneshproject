---
title: How to untar over SSH
author: Danesh Manoharan
date: 2008-01-21T12:40:29+00:00
pvc_views:
  - 19396
dsq_thread_id:
  - 889968875

---
I develop quite a few bash scripts to automated backups and dropbox operation in my office. One of the usual requirements is to tar (tar.gz) the files locally and later untar them on the destination server when needed. I have a few simple scripts with interactive menus which help the data center operations team with their daily backup tasks.

One of the challenges during development was the ability to untar files on the backup server over SSH. The command by default will untar to the home directory instead of the target folder <strike>output always returned success but the files were nowhere to be found</strike>. This apparently is a limitation on the tar command, it did not know where to untar the files to when being executed over SSH. Fortunately the fix was really simple.

Original command,

    ssh 127.0.0.1 'tar zxvf ~/test/files.tzr.gz'

The simple fix,

    ssh 127.0.0.1 'cd ~/test/ ; tar zxvf files.tar.gz'

or, (thanks Aik)

    ssh 127.0.0.1 'tar zxvf files.tar.gz -C ~/test/'

Here's a video I put together to demonstrate the above. Hopefully I got it right.

<!--more-->

[youtube]http://www.youtube.com/watch?v=uyxSmZpbl24[/youtube]

Please drop me a comment if you know a better way.