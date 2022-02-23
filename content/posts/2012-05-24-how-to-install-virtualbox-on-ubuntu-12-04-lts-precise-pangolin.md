---
title: How to install Virtualbox on Ubuntu 12.04 LTS Precise Pangolin
author: Danesh
date: 2012-05-23T21:00:00+00:00
pvc_views:
  - 8306
dsq_thread_id:
  - 889817302

---
<img loading="lazy" src="/wp-content/uploads/2012/05/Virtualbox-4.1_4.1.16-ubuntu-1204-lts1.png" alt="" width="450" height="354" />

1. Download and install Oracle&#8217;s public key.

`danesh@python:~$ wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc -O- | sudo apt-key add -`

2. Create a repo file for Virtualbox

`danesh@python:~$ sudo -s  echo "deb http://download.virtualbox.org/virtualbox/debian precise contrib" >> ~/virtualbox.list`

`danesh@python:~$ sudo mv ~/virtualbox.list /etc/apt/sources.list.d/`

3. Install Virtualbox

`danesh@python:~$ sudo apt-get update`

`danesh@python:~$ sudo apt-get install dkms`

`danesh@python:~$ sudo apt-get install virtualbox-4.1`

<div>
  Enjoy.
</div>