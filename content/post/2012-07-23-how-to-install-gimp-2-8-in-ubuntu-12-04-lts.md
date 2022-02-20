---
title: How to install GIMP 2.8 in Ubuntu 12.04 LTS
author: Danesh
date: 2012-07-23T15:14:09+00:00
url: /posts/how-to-install-gimp-2-8-in-ubuntu-12-04-lts/
pvc_views:
  - 1444
dsq_thread_id:
  - 891153021

---
<a href="/posts/how-to-install-gimp-2-8-in-ubuntu-12-04-lts/gimp-2-8/" rel="attachment wp-att-2959"><img loading="lazy" class="alignnone size-medium wp-image-2959" title="GIMP-2.8" src="/wp-content/uploads/2012/07/GIMP-2.8-450x212.png" alt="" width="450" height="212" srcset="/wp-content/uploads/2012/07/GIMP-2.8-450x212.png 450w, /wp-content/uploads/2012/07/GIMP-2.8.png 505w" sizes="(max-width: 450px) 100vw, 450px" /></a>

The default GIMP package that comes with Ubuntu 12.04 is 2.6. However, if you&#8217;d rather have the latest version 2.8 here&#8217;s how you can get it.

1. Remove the existing GIMP package.

`sudo apt-get autoremove gimp gimp-plugin-registry<br />
`  
2. Add the unofficial GIMP 2.8 PPA

`sudo add-apt-repository ppa:otto-kesselgulasch/gimp<br />
`  
3. Update your sources and install GIMP 2.8 package.

`sudo apt-get update && sudo apt-get install gimp<br />
`