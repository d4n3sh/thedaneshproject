---
title: How to reset your Gnome desktop
author: Danesh
date: 2010-12-19T13:15:42+00:00
url: /posts/how-to-reset-your-gnome-desktop/
pvc_views:
  - 2095
dsq_thread_id:
  - 890980465

---
So you messed up the Gnome desktop and don&#8217;t know how to restore it back to it&#8217;s default settings. Here&#8217;s how with no risks.

1. Log out and then hit &#8220;Ctrl + ALT + F1&#8221; to opening up a terminal.

2. Delete the following directories.

`.gnome .gnome2 .gconf .gconfd .metacity`

Or run the this command.

`rm -rf rm -rf .gnome .gnome2 .gconf .gconfd .metacity`

3. &#8220;Ctrl + ALT + F7/F8&#8221; and log in as usual.

_This guide is based on Ubuntu 10.10_