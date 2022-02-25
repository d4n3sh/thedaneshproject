---
title: Ubuntu 12.04 LTS Unity Launcher bug workaround
author: Danesh
date: 2012-05-15T21:00:31+00:00
pvc_views:
  - 12855
dsq_thread_id:
  - 889899311

---
<a href="/posts/ubuntu-12-04-lts-unity-launcher-bug-workaround/compizconfig-settings-manager-experimental-tab/" rel="attachment wp-att-2479"><img loading="lazy" class="alignnone size-medium wp-image-2479" title="CompizConfig-Settings-Manager-Experimental-Tab" src="/wp-content/uploads/2012/05/CompizConfig-Settings-Manager-Experimental-Tab-450x282.png" alt="" width="450" height="282" srcset="/wp-content/uploads/2012/05/CompizConfig-Settings-Manager-Experimental-Tab-450x282.png 450w, /wp-content/uploads/2012/05/CompizConfig-Settings-Manager-Experimental-Tab.png 992w" sizes="(max-width: 450px) 100vw, 450px" /></a>

The Unity launcher for Ubuntu 12.04 LTS Precise Pangolin has a bug. When auto hide is enabled, there is a lag when trying to get the panel to show. When working correctly the panel should show when the mouse cursor hits the edge but the bug requires you to move your mouse beyond the edge to get the panel to show. Feels heavy.

There's no official fix out at the time of this post. Do you?

Currently, the workaround to get the panel working is through a config tweak using the "compizconfig-settings-manager" tool. Here's how.

1. Download compizconfig-settings-manager tool. Command line or from the app store.

[<img loading="lazy" class="alignnone" title="CompizConfig Settings Manager" src="https://apps.ubuntu.com/assets/images/scbutton-free-200px.png" alt="" width="200" height="60" />][1]

or

`danesh@python:~$ sudo apt-get install compizconfig-settings-manager`

2. Launch the compizconfig-settings-manager. Go to "Desktop &#8211;>  Ubuntu Unity Plugin &#8211;> Experimental Tab".

Change the value for "Launcher Reveal Pressure" to "1" or what works for you. I have mine set at 10.

Enjoy.

 [1]: https://apps.ubuntu.com/cat/applications/compizconfig-settings-manager/