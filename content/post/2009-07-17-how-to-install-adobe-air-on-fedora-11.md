---
title: How to install Adobe AIR on Fedora 11
author: Danesh
date: 2009-07-16T17:24:17+00:00
url: /posts/how-to-install-adobe-air-on-fedora-11/
aktt_notify_twitter:
  - no
pvc_views:
  - 5421
dsq_thread_id:
  - 892561351

---
1. Pull up a console and su as root.

`[danesh@jackal ~]$ su -`

2. Install these packages first.

`[root@jackal ~]# yum -y install xterm gtk2-devel gnome-keyring libxml2-devel libxslt rpm-devel nss`

3. Grab the latest vesion of Adobe AIR from Adobe&#8217;s [download page][1].

`[root@jackal ~]# wget http://airdownload.adobe.com/air/lin/download/latest/AdobeAIRInstaller.bin`

4. Make the .bin file executable by using the chmod command.

`[root@jackal ~]# chmod +x AdobeAIRInstaller.bin`

6. Execute the .bin file.

`[root@jackal ~]# ./AdobeAIRInstaller.bin`

Follow the screens and your install&#8217;s complete.

<div id='gallery-4' class='gallery galleryid-1638 gallery-columns-3 gallery-size-thumbnail'>
  <figure class='gallery-item'> 
  
  <div class='gallery-icon landscape'>
    <a href='/wp-content/uploads/2009/07/Screenshot-Adobe-AIR-Setup-1.png'><img width="150" height="150" src="/wp-content/uploads/2009/07/Screenshot-Adobe-AIR-Setup-1-150x150.png" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" /></a>
  </div></figure><figure class='gallery-item'> 
  
  <div class='gallery-icon landscape'>
    <a href='/wp-content/uploads/2009/07/Screenshot-Adobe-AIR-Setup-2.png'><img width="150" height="150" src="/wp-content/uploads/2009/07/Screenshot-Adobe-AIR-Setup-2-150x150.png" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" /></a>
  </div></figure><figure class='gallery-item'> 
  
  <div class='gallery-icon landscape'>
    <a href='/wp-content/uploads/2009/07/Screenshot-Adobe-AIR-Setup-3.png'><img width="150" height="150" src="/wp-content/uploads/2009/07/Screenshot-Adobe-AIR-Setup-3-150x150.png" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" /></a>
  </div></figure>
</div>

 [1]: http://get.adobe.com/air/