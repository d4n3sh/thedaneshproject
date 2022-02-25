---
title: 'cannot perform readlinkat() on the mount namespace file descriptor of the init process: Permission denied'
author: Danesh Manoharan
date: 2018-08-18T19:00:48+00:00

---
Installed kernel 4.18 on my Ubuntu recently, since then snap packages broke with the following error.

It has something to do with the AppArmor exception rule for ptrace for what I could gather.

<pre class="toolbar-overlay:false nums:false lang:sh decode:true ">danesh@hades:$ spotify
cannot perform readlinkat() on the mount namespace file descriptor of the init process: Permission denied</pre>

The workaround for now is to upgrade your snap core to the beta channel.

<pre class="nums:false lang:sh decode:true ">danesh@hades:~/kernel$ sudo snap refresh --channel=beta core</pre>

 