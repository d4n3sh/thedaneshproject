---
title: Gnome online accounts not working
author: Danesh
date: 2014-01-08T15:58:18+00:00
dsq_thread_id:
  - 2100332514

---
<a href="/posts/gnome-online-accounts-working/gnome-online-accounts-jan082014/" rel="attachment wp-att-3407"><img loading="lazy" class="alignnone size-medium wp-image-3407" alt="gnome-online-accounts-Jan082014" src="/wp-content/uploads/2014/01/gnome-online-accounts-Jan082014-450x250.jpg" width="450" height="250" srcset="/wp-content/uploads/2014/01/gnome-online-accounts-Jan082014-450x250.jpg 450w, /wp-content/uploads/2014/01/gnome-online-accounts-Jan082014.jpg 615w" sizes="(max-width: 450px) 100vw, 450px" /></a>

Just completed my fresh install of Arch Linux and Gnome 3.10. Hit my first issue, gnome-online-accounts dialog does not come up so I can&#8217;t add my clound accounts.

The Fix:

Install &#8220;telepathy-gaze&#8221; packge.

`pacman -S telepathy-gaze`