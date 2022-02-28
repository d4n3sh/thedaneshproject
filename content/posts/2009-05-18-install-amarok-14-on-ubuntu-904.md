---
title: Install Amarok 1.4 on Ubuntu 9.04
author: Danesh Manoharan
date: 2009-05-17T17:42:31+00:00
aktt_notify_twitter:
  - no
pvc_views:
  - 40702
dsq_thread_id:
  - 890828845

---
![](http://farm4.static.flickr.com/3337/3538709803_e69c07498a_t.jpg)

Been using Jaunty since it came out. Loving the speed, simplicity and estatics!!

Everything works well except for Amarok 2 which ships default with Jaunty. I've been an Amarok 1.4 user for a long time now, moving to Amarok 2 is not something I fancy doing right now. Fortunately getting Amarok 1.4 onto Ubuntu is easy. Here's how;

Create a new source file in "/etc/apt/sources.list.d/" and call it "amarok14.list".

`root@jackal:/# touch /etc/apt/sources.list.d/amarok14.list`

Add these 2 lines to the source file. You can either copy & paste or run the echo command seen below.

`deb <a class="linkification-ext" title="Linkification: http://ppa.launchpad.net/bogdanb/ppa/ubuntu" href="http://ppa.launchpad.net/bogdanb/ppa/ubuntu">http://ppa.launchpad.net/bogdanb/ppa/ubuntu</a> jaunty main<br />
deb-src <a class="linkification-ext" title="Linkification: http://ppa.launchpad.net/bogdanb/ppa/ubuntu" href="http://ppa.launchpad.net/bogdanb/ppa/ubuntu">http://ppa.launchpad.net/bogdanb/ppa/ubuntu</a> jaunty main`

`root@jackal:/# echo "deb <a class="linkification-ext" title="Linkification: http://ppa.launchpad.net/bogdanb/ppa/ubuntu" href="http://ppa.launchpad.net/bogdanb/ppa/ubuntu">http://ppa.launchpad.net/bogdanb/ppa/ubuntu</a> jaunty main" >> /etc/apt/sources.list.d/amarok14.list<br />
root@jackal:/# echo "deb-src <a class="linkification-ext" title="Linkification: http://ppa.launchpad.net/bogdanb/ppa/ubuntu" href="http://ppa.launchpad.net/bogdanb/ppa/ubuntu">http://ppa.launchpad.net/bogdanb/ppa/ubuntu</a> jaunty main" >> /etc/apt/sources.list.d/amarok14.list`

Make sure to register the PPA GPG key.

`root@jackal:/# sudo apt-key adv --recv-keys --keyserver keyserver.ubuntu.com 0x1d7e9dd033e89ba781e32a24b9f1c432ae74ae63`

Update your sources.

`root@jackal:/# apt-get update`

Remove any old instance of Amarok

`root@jackal:/# apt-get remove amarok`

Install Amarok 1.4

`root@jackal:/# apt-get install amarok14`

That's it. Buzz me if it doesn't work.