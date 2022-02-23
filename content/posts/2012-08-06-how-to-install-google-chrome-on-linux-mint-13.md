---
title: How to install Google Chrome on Linux Mint 13
author: Danesh
date: 2012-08-06T15:22:14+00:00
pvc_views:
  - 3381
dsq_thread_id:
  - 889772961

---
Here&#8217;s how to install Google Chrome on Linux Mint 12 &#8220;Maya&#8221;.

1. Download the signing key.

`wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -<br />
`  
2. Download the install package. Beta or Stable

Beta,

`wget https://dl.google.com/linux/direct/google-chrome-beta_current_amd64.deb<br />
`  
Stable,

`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb<br />
`  
3. Install the Google Chrome package. This will also automatic add the Google Chrome repositories which will allow Google Chrome to receive updates.

`sudo dpkg -i google-chrome-beta_current_amd64.deb<br />
`  
Enjoy your browser. 😀