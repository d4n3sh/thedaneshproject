---
title: 'cannot perform readlinkat() on the mount namespace file descriptor of the init process: Permission denied'
author: Danesh Manoharan
date: 2018-08-18T19:00:48+00:00

---
Installed kernel 4.18 on my Ubuntu recently, since then snap packages broke with the following error.

It has something to do with the AppArmor exception rule for ptrace for what I could gather.

```
danesh@hades:$ spotify
cannot perform readlinkat() on the mount namespace file descriptor of the init process: Permission denied
```

The workaround for now is to upgrade your snap core to the beta channel.

```
danesh@hades:~/kernel$ sudo snap refresh --channel=beta core
```

 