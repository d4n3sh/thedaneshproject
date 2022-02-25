---
title: How to find the number of physical CPUs in Linux
author: Danesh Manoharan
date: 2009-01-14T09:52:29+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 29028
dsq_thread_id:
  - 889779954

---
With multicore CPUs it's easy for newbies to get confused when faced with questions like;

1. How many physical CPUs does the server have?

2. How many cores on each CPU? Duo/Quad

In Linux it's actually quite easy to get this info.

You could go through the /var/log/dmesg file or the /proc/cpuinfo file. For this tutorial we'll look at the /proc/cpuinfo file.

**Physical CPU count?**

Run "cat /proc/cpuinfo | grep "physical id" | sort | uniq | wc -l".

[root@bender ~]# cat /proc/cpuinfo | grep "physical id" | sort | uniq | wc -l  
2

**How many cores?**

Run **"**cat /proc/cpuinfo | grep "cpu cores" | uniq".

[root@kmigb000 ~]# cat /proc/cpuinfo | grep "cpu cores" | uniq  
cpu coresÂ Â Â Â Â Â  : 2

2 mean that each physical CPU has 2 cores on it. If cpu cores was 1 then the CPU's single core.

**How many virtual processors?**

Run "cat /proc/cpuinfo | grep "^processor""

[root@bender ~]# cat /proc/cpuinfo | grep "^processor"  
processorÂ Â Â Â Â Â  : 0  
processorÂ Â Â Â Â Â  : 1  
processorÂ Â Â Â Â Â  : 2  
processorÂ Â Â Â Â Â  : 3

That's about right, 2 physical CPUs x 2 cores each = 4 virtual processeors.

However, it's a bit different for HT (Hyper-Threading). If you get cpu core = 1 but the virtual processors = 2 then the CPU's running HT. HT will only work with the SMP kernel.