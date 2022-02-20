---
title: 'Linux Tip #9: Create multiple folder or files'
author: Danesh
date: 2009-07-02T00:00:00+00:00
url: /posts/linux-tip-9-create-multiple-folder-or-files/
aktt_notify_twitter:
  - no
pvc_views:
  - 3950
dsq_thread_id:
  - 892113010

---
Sometime it’s necessary for you to create multiple folders or files. This is normally the case for me when I’m working with the clusters at my work place. Fortunately, In Linux this is easy.

Using the “for loop”, one could easily put together a one-liner to see results. See sample below.

The initial “ls” shows that the directory is empty.  
`<br />
[root@abubu test]# ls -l<br />
total 0`

Now, make the magic happens. Run “for ((i=1;i<=10;i++)); do mkdir ./folder-$i; done”

`[root@abubu test]# for ((i=1;i<=10;i++)); do mkdir ./folder-$i; done`

Now, “ls” will give you 10 folders. 😉

`[root@abubu test]# ls -l<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-1<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-10<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-2<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-3<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-4<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-5<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-6<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-7<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-8<br />
drwxr-xr-x 2 root root 4096 Jun 30 15:49 folder-9<br />
total 40<br />
[root@abubu test]#`

This is just one way to do this. Please feel free to comment if you know a better way.