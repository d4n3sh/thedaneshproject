---
title: How to install Adobe AIR on Fedora 12
author: Danesh Manoharan
date: 2010-04-27T23:30:37+00:00
pvc_views:
  - 3027
dsq_thread_id:
  - 891834864

---
1. Pull up a console and su to root.

`[danesh@jackal ~]$ su -`

2. Grab the latest vesion of Adobe AIR from Adobe's [download page][1].

`<span>[root@jackal ~]# wget  <a href="http://airdownload.adobe.com/air/lin/download/latest/AdobeAIRInstaller.bin">http://airdownload.adobe.com/air/lin/download/latest/AdobeAIRInstaller.bin</a></span>`

3. Make the .bin file executable by using the chmod command.

`[root@jackal ~]# chmod +x AdobeAIRInstaller.bin`

4. Execute the .bin file.

`[root@jackal ~]# ./AdobeAIRInstaller.bin`

Follow the screens and your install's complete.

NOTE:

If you get errors when trying to run AIR apps try the below;

1. delete /etc/opt/adobe/......../crypt/

2. if  Tweetdeck fails to launch, make sure kwallet is running.

![][2]

 [1]: http://get.adobe.com/air/
 [2]: /wp-includes/js/tinymce/plugins/wpgallery/img/t.gif "gallery link="file""