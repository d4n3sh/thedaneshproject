---
title: How to enable DMA in Linux
author: Danesh
date: 2007-09-20T17:06:16+00:00
pvc_views:
  - 16899
dsq_thread_id:
  - 889737787

---
While loading [K3b][1] to burn a DVD earlier today I received a warning that my DMA support had been turned off and write speeds would be slow. DMA is normally enabled by default, provided the disk supports it and is handled by the OS.

![][2] 

**What is DMA?**

DMA (Direct Memory Access) is the mechanism which allow your disk device to move data directly to memory without passing through the CPU. This shortens the distance the data needs to travel and reduces the load on the CPU thus improving performance and quality of the data. DMA eliminates errors that might occur when data is passed through the CPU. For example, you might hear pops and click while playing an audio CD or your video quality might be distorted when reading directly from a cdrom/dvd drive with DMA turned off.

I will have to investigate what happen later. But for now this is how I enabled DMA support for the DVD+-drive the manual way.<!--more-->

1. Locate my DVD +- drive

> \# sudo su &#8211; / su &#8211; (change user to root)
> 
> \# ls -l /dev/dvdrecorder
> 
> \# lrwxrwxrwx 1 root root 3 Sep 19 16:38 /dev/dvdrecorder -> hda

2. Check if DMA is on/off

> \# hdparm -d /dev/hda:  
> using_dma = 0 (off)

3. Turn DMA on

> \# hdparm -d 1 /dev/hda
> 
> /dev/hda:  
> setting using_dma to 1 (on)  
> using_dma = 1 (on)

 [1]: http://www.google.com/url?sa=t&ct=res&cd=1&url=http%3A%2F%2Fk3b.plainblack.com%2F&ei=JajyRqmCOKTCgQPa2d2QBA&usg=AFQjCNHnlacA3NccoXPjdhymYM5l6xu8GA&sig2=psTGSoQ1O7ptA2_eQ7etCg
 [2]: http://img229.imageshack.us/img229/7562/k3bhdparmin9.jpg