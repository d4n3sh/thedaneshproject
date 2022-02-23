---
title: How to find the number of physical CPUs in Linux
author: Danesh
date: 2009-01-14T09:52:29+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 29028
dsq_thread_id:
  - 889779954

---
With multicore CPUs it&#8217;s easy for newbies to get confused when faced with questions like;

1. How many physical CPUs does the server have?

2. How many cores on each CPU? Duo/Quad

In Linux it&#8217;s actually quite easy to get this info.

You could go through the /var/log/dmesg file or the /proc/cpuinfo file. For this tutorial we&#8217;ll look at the /proc/cpuinfo file.

**Physical CPU count?**

Run &#8220;cat /proc/cpuinfo | grep &#8220;physical id&#8221; | sort | uniq | wc -l&#8221;.

[root@bender ~]# cat /proc/cpuinfo | grep &#8220;physical id&#8221; | sort | uniq | wc -l  
2

**How many cores?**

Run **&#8220;**cat /proc/cpuinfo | grep &#8220;cpu cores&#8221; | uniq&#8221;.

[root@kmigb000 ~]# cat /proc/cpuinfo | grep &#8220;cpu cores&#8221; | uniq  
cpu coresÂ Â Â Â Â Â  : 2

2 mean that each physical CPU has 2 cores on it. If cpu cores was 1 then the CPU&#8217;s single core.

**How many virtual processors?**

Run &#8220;cat /proc/cpuinfo | grep &#8220;^processor&#8221;&#8221;

[root@bender ~]# cat /proc/cpuinfo | grep &#8220;^processor&#8221;  
processorÂ Â Â Â Â Â  : 0  
processorÂ Â Â Â Â Â  : 1  
processorÂ Â Â Â Â Â  : 2  
processorÂ Â Â Â Â Â  : 3

That&#8217;s about right, 2 physical CPUs x 2 cores each = 4 virtual processeors.

However, it&#8217;s a bit different for HT (Hyper-Threading). If you get cpu core = 1 but the virtual processors = 2 then the CPU&#8217;s running HT. HT will only work with the SMP kernel.