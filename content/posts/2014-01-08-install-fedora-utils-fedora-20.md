---
title: How to install Fedora Utils on Fedora 20
author: Danesh Manoharan
date: 2014-01-08T07:41:38+00:00
---
![fedorautils-08Jan2014](/wp-content/uploads/2014/01/fedorautils-08Jan2014.png)

Fedora Utils is the "[Ubuntu Tweak][1]" of Fedora. It simplifies many of the post install tasks. It's basically a collection of scripts and customizable plugins wrapped around a nice GUI which  help you install fonts, codecs, flash, java, etc. It also cleans up your system, fixes some common issues, tweaks your desktop, etc.

Here's a one liner to get it installed on your Fedora 20.

`su -c "cd /tmp/ && curl http://satya164.github.io/fedorautils/fedorautils-installer -o fedorautils-installer && chmod +x fedorautils-installer && ./fedorautils-installer"`

Source: [Fedora Utils][2]

 [1]: http://ubuntu-tweak.com/
 [2]: http://satya164.github.io/fedorautils/
