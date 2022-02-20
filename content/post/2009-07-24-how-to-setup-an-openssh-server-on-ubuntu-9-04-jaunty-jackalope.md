---
title: How to setup an OpenSSH Server on Ubuntu 9.04 Jaunty Jackalope
author: Danesh
date: 2009-07-23T17:08:29+00:00
url: /posts/how-to-setup-an-openssh-server-on-ubuntu-9-04-jaunty-jackalope/
aktt_notify_twitter:
  - no
pvc_views:
  - 14309
dsq_thread_id:
  - 889970369

---
Here&#8217;s a simple walkthrough to setup an OpenSSH server on Jaunty together with 2 basic hardening options you should apply.

1. Install the OpenSSH server.

Fire up a console and run the command below. This will install the required binaries and packages for the OpenSSH server.

`apt-get install openssh-server`

2. Get some basic hardening in by disabling &#8220;root&#8221; login and restricting access to specific accounts. All changes are to the &#8220;/etc/ssh/sshd_config&#8221; configuration file.

vi the &#8220;/etc/ssh/sshd_config&#8221; file and apply the changes below.

Look for `"PermitRootLogin yes"`  
and change it to  
`"PermitRootLogin no"`

Start a new line and add the line below. &#8220;danesh&#8221; is my user name, you should replace it with your own user name. You can add multiple user names by seperating each user name with a space. 

`AllowUsers danesh user1 user2`

3. Restart your shiny new OpenSSH server and you are good to go.

Run the command below to restart the OpenSSH server.

`sudo /etc/init.d/ssh restart`