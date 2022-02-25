---
title: Password protect single user mode
author: Danesh
date: 2007-11-12T09:53:04+00:00
pvc_views:
  - 19416
dsq_thread_id:
  - 889736472

---
You forget your root password and get locked out of your own box. What do you do? Typically, you would reboot into single user mode and change the password there.

When booting into single user mode you will not be prompted for the root password. This is something every attacker knows and prays on once he has gained physical access to you box. So what do you do?

Firstly, a good sys admin knows not to forget the root password. Login in as root is never a good idea so using _**sudo**_ is always advised. This still leaves the single user mode vulnerable, to secure it you will have to append the following line "_**su:S:wait:/sbin/sulogin**_" to your "_**/etc/inittab**_" file. Now, every time you boot into single user mode you will be prompted for the root password.

See sample below,

> \# password protect single user mode  
> su:S:wait:/sbin/sulogin

PS: Always remember you password, if you can't then write in down in a safe place.