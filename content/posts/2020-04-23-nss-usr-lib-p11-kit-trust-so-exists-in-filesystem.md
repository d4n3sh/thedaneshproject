---
title: 'nss: /usr/lib/p11-kit-trust.so exists in filesystem'
author: Danesh Manoharan
date: 2020-04-23T10:18:20+00:00

---
My Arch update broke today with the following error which was due to a missing soname entry in the older nss packages. 

The error was identified and a post describing the error with a fix was posted to the ArchLinux news feed. [Read Here][1] 

```
? sudo pacman -Syu                          
.....
.....
(201/201) checking for file conflicts                                                                  [------------------------------------------------------------] 100%
error: failed to commit transaction (conflicting files)
nss: /usr/lib/p11-kit-trust.so exists in filesystem
lib32-nss: /usr/lib32/p11-kit-trust.so exists in filesystem
Errors occurred, no packages were upgraded.
```

```
? pacman -Syu --overwrite /usr/lib\*/p11-kit-trust.so
.....
.....

? sudo pacman -Syu                                        
:: Synchronizing package databases...
 core is up to date
 extra is up to date
 community is up to date
 multilib is up to date
 endeavouros is up to date                                                   0.0   B  0.00   B/s 00:00 [c  o  o  o  o  o  o  o  o  o  o  o  o  o  o  o  o  o  o  o  ]   0%
:: Starting full system upgrade...
 there is nothing to do
```

 [1]: https://www.archlinux.org/news/nss3511-1-and-lib32-nss3511-1-updates-require-manual-intervention/