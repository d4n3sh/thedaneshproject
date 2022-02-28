---
title: How to install Dropbox in Ubuntu 8.10
author: Danesh Manoharan
date: 2009-01-05T13:39:48+00:00
pvc_views:
  - 21408
robotsmeta:
  - index,follow
dsq_thread_id:
  - 892494682

---
![](/wp-content/uploads/2009/01/dropbox_logo.png)

[Dropbox][1] is my favorite online storage solution. Here's how to install it on Ubuntu 8.10 Interpid

1. Add the Dropbox repository for Ubuntu package source file. I use **/etc/apt/source.list.d/dropbox.list** file.

`deb http://linux.getdropbox.com/ubuntu intrepid main<br />
deb-src http://linux.getdropbox.com/ubuntu intrepid main`

Either manually add the lines above to the **/etc/apt/source.list.d/dropbox.list** file or run the commands below to do the same.

`root@dingo:~# echo "deb http://linux.getdropbox.com/ubuntu intrepid main" >> /etc/apt/sources.list.d/dropbox.list<br />
root@dingo:~# echo "deb-src http://linux.getdropbox.com/ubuntu intrepid main" >> /etc/apt/sources.list.d/dropbox.list<br />
root@dingo:~# cat /etc/apt/sources.list.d/dropbox.list`

2. Update your packages list. Run "**apt-get update**".

`root@dingo:~# apt-get update<br />
.............<br />
...........<br />
.............<br />
Ign http://linux.getdropbox.com intrepid Release.gpg<br />
Ign http://linux.getdropbox.com intrepid/main Translation-en_US<br />
Ign http://linux.getdropbox.com intrepid Release<br />
Ign http://linux.getdropbox.com intrepid/main Packages<br />
Ign http://linux.getdropbox.com intrepid/main Sources<br />
Get:1 http://linux.getdropbox.com intrepid/main Packages [622B]<br />
Get:2 http://linux.getdropbox.com intrepid/main Sources [537B]<br />
.................<br />
..............<br />
Fetched 1160B in 59s (20B/s)<br />
Reading package lists... Done`

3. Install Dropbox  
`<br />
` `root@dingo:~#` `apt-get install nautilus-dropbox`

.......  
.......  
.......  
Setting up nautilus-dropbox (0.5.0-1) ...

4. Restart nautilus to start Dropbox. You will see a new Dropbox icon in your system tray. Right click on it and select "**start dropbox**". The daemon will download the binaries required and start the registration process.

`root@dingo:~# killall nautilus`

That's it. Enjoy this get service.

Buzz me if you need help...

 [1]: http://getdropbox.com