---
title: How to install Virtualbox on Ubuntu 12.04 LTS Precise Pangolin
author: Danesh Manoharan
date: 2012-05-23T21:00:00+00:00
---
![](/wp-content/uploads/2012/05/Virtualbox-4.1_4.1.16-ubuntu-1204-lts1.png)

1. Download and install Oracle's public key.

`danesh@python:~$ wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc -O- | sudo apt-key add -`

2. Create a repo file for Virtualbox

`danesh@python:~$ sudo -s  echo "deb http://download.virtualbox.org/virtualbox/debian precise contrib" >> ~/virtualbox.list`

`danesh@python:~$ sudo mv ~/virtualbox.list /etc/apt/sources.list.d/`

3. Install Virtualbox

`danesh@python:~$ sudo apt-get update`

`danesh@python:~$ sudo apt-get install dkms`

`danesh@python:~$ sudo apt-get install virtualbox-4.1`

Enjoy.
