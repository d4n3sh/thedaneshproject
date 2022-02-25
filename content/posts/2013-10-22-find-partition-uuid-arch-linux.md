---
title: How to find partition UUID on Arch Linux
author: Danesh Manoharan
date: 2013-10-22T15:31:07+00:00
dsq_thread_id:
  - 1887215485

---
Using UUID to identify you partitions is better then using kernel device names .i.e /dev/sd?. Mainly on systems where drives get move around frequently. Dev names change when the physical order of the drives are change but the UUID always remains the same. 

You can use the "lsblk" or "blkid" command to get the UUID of your partitions. In this case I'm running it on my Arch Linux box.

`[root@r2d2 ~]# lsblk -no NAME,UUID /dev/sdb1<br />
sdb1 eb2cb768-7306-4fe5-a981-14d27d0c25fa`

`[root@r2d2 ~]# lsblk -no NAME,UUID<br />
sda1 05df7ca0-4af7-4e0a-ae1b-72518966847c<br />
sda2 8ad2ec57-2d62-482b-96ff-253fa402c786<br />
sdb1 eb2cb768-7306-4fe5-a981-14d27d0c25fa<br />
sdc1 cba2f94f-3eb4-4d6b-af7d-5d947eec2209`

`[root@r2d2 ~]# lsblk -f<br />
NAME   FSTYPE LABEL UUID                                 MOUNTPOINT<br />
sda1 ext4         05df7ca0-4af7-4e0a-ae1b-72518966847c /<br />
sda2 swap         8ad2ec57-2d62-482b-96ff-253fa402c786 [SWAP]<br />
sdb1 ext4         eb2cb768-7306-4fe5-a981-14d27d0c25fa /vm<br />
sdc1 ext4         cba2f94f-3eb4-4d6b-af7d-5d947eec2209` 

`[root@r2d2 ~]# blkid -o list<br />
device                       fs_type       label   mount point         UUID<br />
------------------------------------------------------------------------------------------------------------<br />
/dev/sdb1                    ext4                  /vm                 eb2cb768-7306-4fe5-a981-14d27d0c25fa<br />
/dev/sdc1                    ext4                  (not mounted)       cba2f94f-3eb4-4d6b-af7d-5d947eec2209<br />
/dev/sda1                    ext4                  /                   05df7ca0-4af7-4e0a-ae1b-72518966847c<br />
/dev/sda2                    swap                  <swap>              8ad2ec57-2d62-482b-96ff-253fa402c786<br />
/dev/sda3                                          (not mounted)`