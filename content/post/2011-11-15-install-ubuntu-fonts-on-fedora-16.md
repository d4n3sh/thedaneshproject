---
title: Install Ubuntu Fonts on Fedora 16
author: Danesh
date: 2011-11-14T17:55:27+00:00
url: /posts/install-ubuntu-fonts-on-fedora-16/
pvc_views:
  - 15399
dsq_thread_id:
  - 889863674

---
1. Let&#8217;s work from your Downloads folder.  
`cd ~/Downloads`  
2. Download the Ubuntu Fonts package from Ubuntu.  
`wget http://font.ubuntu.com/download/ubuntu-font-family-0.80.zip`  
3. Extra the downloaded zip file.  
`unzip ubuntu-font-family-0.80.zip`  
4. Rename the extracted directory. (Not a must)  
`mv ubuntu-font-family-0.80 ubuntu-font-family`  
5. Copy the extracted directory to the system shared fonts directory.  
`su -c 'cp -rv  ubuntu-font-family /usr/share/fonts/'`  
6. Set the permissions for the directory you just moved.  
`su -c 'chmod 755 /usr/share/fonts/ubuntu-font-family'`  
7. Scan and build the fonts cache files for the new Ubuntu files.  
cd /usr/share/fonts  
su -c &#8216;fc-cache ubuntu-font-family&#8217;

That&#8217;s it, you should now be able to use the Ubuntu fonts in your applications and documents. 

Here&#8217;s a video of the process.  
[How To install Ubuntu Fonts on Fedora 16][1]

 [1]: http://www.youtube.com/watch?v=-OYU7AZ09JE