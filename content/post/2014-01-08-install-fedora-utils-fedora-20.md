---
title: How to install Fedora Utils on Fedora 20
author: Danesh
date: 2014-01-08T07:41:38+00:00
url: /posts/install-fedora-utils-fedora-20/
dsq_thread_id:
  - 2098200185

---
<a href="/posts/install-fedora-utils-fedora-20/fedorautils-08jan2014/" rel="attachment wp-att-3402"><img loading="lazy" class="alignnone size-full wp-image-3402" alt="fedorautils-08Jan2014" src="/wp-content/uploads/2014/01/fedorautils-08Jan2014.png" width="365" height="358" /></a>

Fedora Utils is the &#8220;[Ubuntu Tweak][1]&#8221; of Fedora. It simplifies many of the post install tasks. It&#8217;s basically a collection of scripts and customizable plugins wrapped around a nice GUI which  help you install fonts, codecs, flash, java, etc. It also cleans up your system, fixes some common issues, tweaks your desktop, etc.

Here&#8217;s a one liner to get it installed on your Fedora 20.

`su -c "cd /tmp/ && curl http://satya164.github.io/fedorautils/fedorautils-installer -o fedorautils-installer && chmod +x fedorautils-installer && ./fedorautils-installer"`

Source: [Fedora Utils][2]

 [1]: http://ubuntu-tweak.com/
 [2]: http://satya164.github.io/fedorautils/