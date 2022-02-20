---
title: How to install Android’s Roboto font in Fedora 16
author: Danesh
date: 2012-01-31T17:16:36+00:00
url: /posts/how-to-install-androids-roboto-font-in-fedora-16/
pvc_views:
  - 3978
dsq_thread_id:
  - 890344543

---
I love the new Android Roboto font family and it looks good on my Fedora 16 install. Here&#8217;s how you can get it into your Fedora 16.

1. Change to root user  
`# su -<br />
` 2. Create the the roboto directory  
`# cd /usr/share/fonts/<br />
# mkdir roboto<br />
# cd roboto`  
3. Download the roboto font and install it.  
`# wget http://www.fontsquirrel.com/fonts/download/roboto -O roboto.zip<br />
# unzip roboto.zip<br />
# rm roboto.zip<br />
# fc-cache /usr/share/fonts/roboto/`

Enjoy your new Roboto fonts!