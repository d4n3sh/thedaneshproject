---
title: Mounting CIFS shares
author: Danesh
date: 2007-08-12T18:26:06+00:00
pvc_views:
  - 6795
dsq_thread_id:
  - 889812823

---
I was playing around with Samba and CIFS mounts last night.

I needed to mount a directory on my openSUSE 10.2 box to my samba server where all my mp3 are stored. Since smbfs will be dropped soon I decided to go with CIFS. Note, smbfs will depreciated starting with kernel version 2.6.20.

There are 2 ways to mount, examples below.

The first method shown below is normally used for temporary mounts. Mounts will be discarded upon reboot or execution of the _**umount**_ command.

> `mount -t cifs -o rw,guest,noperm //10.0.0.200/Mp3    /mnt/mp3 umount` 
> 
> `/mnt/mp3 (this will unmount)<br />
` 

If you are looking for a permanent mount, you will need to add the following line into your /etc/fstab file.

> `//10.0.0.200/Mp3        /mnt/mp3      cifs    rw,guest,noperm`

Options I used for my mounts,

rw - read write access. My shares are public so everyone has read/write access.  
guest - no password prompt.

noperm - client does not perform permission checks. Needed if uid and gid are not the same on client and server.

Sources:

[Linux CIFS client guide by Steve French][1]

 [1]: http://pserver.samba.org/samba/ftp/cifs-cvs/linux-cifs-client-guide.pdf