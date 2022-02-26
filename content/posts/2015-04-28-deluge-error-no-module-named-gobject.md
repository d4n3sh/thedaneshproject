---
title: Deluge Error. No module named gobject
author: Danesh Manoharan
date: 2015-04-28T14:07:05+00:00
dsq_thread_id:
  - 3719709222

---
![No module named gobject](/wp-content/uploads/2015/04/Deluge-No-module-named-gobject-error-450x105.png)

I just installed Deluge on Archlinux but the GUI kept failing to come up with  "No module named gobject".

This happens because installing just the deluge package does not meet all the dependencies required to run the GUI. Install "python-gobject2" and "pygtk" packages to satisfy the dependencies and Deluge will run fine.

`$pacman -Sy python-gobject2 pygtk`
