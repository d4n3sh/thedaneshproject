---
title: Install latest Ansible on Ubuntu
author: Danesh Manoharan
date: 2018-08-14T17:48:08+00:00

---
Steps to get the latest version of Ansible installed on Ubuntu or any Ubuntu variant. In my case Kubuntu 18.04.1.

<pre class="nums:false tab-convert:true lang:sh decode:true ">danesh@hades:~$ sudo apt-get update
danesh@hades:~$ sudo apt-get install software-properties-common
danesh@hades:~$ sudo apt-add-repository ppa:ansible/ansible
danesh@hades:~$ sudo apt-get update
danesh@hades:~$ sudo apt-get install ansible
danesh@hades:~$ ansible --version
ansible 2.6.2
config file = /etc/ansible/ansible.cfg
configured module search path = [u'/home/danesh/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
ansible python module location = /usr/lib/python2.7/dist-packages/ansible
executable location = /usr/bin/ansible
python version = 2.7.15rc1 (default, Apr 15 2018, 21:51:34) [GCC 7.3.0]
```