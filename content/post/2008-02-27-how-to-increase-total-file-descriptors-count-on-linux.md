---
title: How to increase file descriptors max limit on Linux
author: Danesh
date: 2008-02-27T11:55:32+00:00
url: /posts/how-to-increase-total-file-descriptors-count-on-linux/
pvc_views:
  - 67569
dsq_thread_id:
  - 889806578

---
Today my DBA reported that the server she was working on was spitting out &#8220;too many open files&#8221; errors and no new processes could be started.

This is a common problem with DB servers with heavy transactions. In my environment there are 6 DB instances running on the server. No quite the optimized setup I would say.

The fix was to increase the total file descriptors kernel parameter count in the /etc/sysctl.conf file. I doubled my limit from 8192 to 16384.

The walk through,

1. Find out what the current open file descriptor limit is.

    ~# more /proc/sys/fs/file-max
    
    ~# 8192
    

or

    ~# sysctl -a | grep fs.file-max
    
    ~# fs.file-max = 8192

2. View how many open file descriptors are currently being used.

    ~# more /proc/sys/fs/file-nr
    
    ~# 8191

3. View how many files are open. The number returned might defer as 1 file descriptor can have multiple open files attached to it.

    ~# lsof | wc -l
    
    ~# 10325

4. Edit the kernel paramneter file /etc/sysctl.conf and add line &#8220;fs.file-max=[new value]&#8221; to it.

    ~# vi /etc/sysctl.conf
    
    fs.file-max = 331287

5. Apply the changes.

    ~# sysctl -p
    ~# fs.file-max = 331287

Problem fixed.