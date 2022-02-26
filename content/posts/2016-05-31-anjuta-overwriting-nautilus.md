---
title: Anjuta overwriting Nautilus
author: Danesh Manoharan
date: 2016-05-31T14:26:40+00:00
dsq_thread_id:
  - 4872172557

---
For some reason Anjuta decided to overwrite Nautilus for all file operations on my Arch Linux box. Every time I'd try to open a file or folder Anjuta would pop up instead.

Fortunately, the fix is easy, just run the command shown below. This will default file operations back to Nautilus.

<pre class="theme:terminal lang:default decode:true">xdg-mime default org.gnome.Nautilus.desktop inode/directory
```