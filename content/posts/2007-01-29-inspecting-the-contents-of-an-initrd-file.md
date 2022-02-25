---
title: Inspecting the contents of an initrd file.
author: Danesh Manoharan
date: 2007-01-29T09:01:18+00:00
pvc_views:
  - 5112
dsq_thread_id:
  - 893704804

---
Today's kernels are moving towards initramfs type initrd files. Initramfs is basicly a cpio archive so all we have to do is uncompress it's contents to a temp folder.

The example below uses the file initrd.SLES10.x64.img from a SLES 10 implementaion.

**#create a temp directory**  
>mkdir /tmp/initramfstmp  
>cd /tmp/initramfstmp

**#copy the initrd file to the temp folder**  
>cp initrd.SLES10.x64 /tmp/initramfstmp/initrd.SLES10.x64.img.gz

**#uncompress the image file**  
>gunzip -v /tmp/initramfstmp/initrd.SLES10.x64.img.gz

**#extract the contents of the cpio archive**  
>cpio -i < /tmp/initramfstmp/initrd.SLES10.x64.img

**#list directory**  
>ls -l  
View actually out put on next page:

<!--more-->

pandora:/tmp # mkdir /tmp/initramfstmp/  
pandora:/tmp # cp /media/DELLBOOT/boot/grub/initrd.SLES10.x64 /tmp/initramfstmp/initrd.SLES10.x64.img.gz  
pandora:/tmp # cd /tmp/initramfstmp/  
pandora:/tmp/initramfstmp # ls  
initrd.SLES10.x64.img.gz  
pandora:/tmp/initramfstmp # gunzip -v initrd.SLES10.x64.img.gz  
initrd.SLES10.x64.img.gz: 64.5% — replaced with initrd.SLES10.x64.img  
pandora:/tmp/initramfstmp # cpio -i < initrd.SLES10.x64.img  
47264 blocks  
pandora:/tmp/initramfstmp # ls -la  
total 25044  
drwxr-xr-x 17 root root 4096 Jan 29 16:53 .  
drwxrwxrwt 50 root root 12288 Jan 29 16:52 ..  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 bin  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 dev  
-rw-r-r- 1 root root 10761 Jan 29 16:53 devz  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 download  
drwxr-xr-x 8 root root 4096 Jan 29 16:53 etc  
-rwxr-xr-x 1 root root 649704 Jan 29 16:53 init  
-rwxr-xr-x 1 root root 652544 Jan 29 16:53 init.old  
-rwxr-xr-x 1 root root 24199168 Jan 29 16:52 initrd.SLES10.x64.img  
-rw-r-r- 1 root root 5604 Jan 29 16:53 installkey.gpg  
drwxr-xr-x 5 root root 4096 Jan 29 16:53 lib  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 lib64  
-rw-r-r- 1 root root 289 Jan 29 16:53 linuxrc.config  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 mnt  
lrwxrwxrwx 1 root root 45 Jan 29 16:53 modules -> lib/modules/2.6.16.21-override-default/initrd  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 mounts  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 proc  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 root  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 sbin  
drwxr-xr-x 2 root root 4096 Jan 29 16:53 sys  
drwxrwxrwt 2 root root 4096 Jan 29 16:53 tmp  
drwxr-xr-x 6 root root 4096 Jan 29 16:53 usr  
drwxr-xr-x 11 root root 4096 Jan 29 16:53 var  
pandora:/tmp/initramfstmp # pwd  
/tmp/initramfstmp