---
title: Deluge Error. No module named gobject
author: Danesh
date: 2015-04-28T14:07:05+00:00
url: /posts/deluge-error-no-module-named-gobject/
dsq_thread_id:
  - 3719709222

---
<figure id="attachment_3540" aria-describedby="caption-attachment-3540" style="width: 450px" class="wp-caption alignnone"><img loading="lazy" class="size-medium wp-image-3540" src="/wp-content/uploads/2015/04/Deluge-No-module-named-gobject-error-450x105.png" alt="No module named gobject" width="450" height="105" srcset="/wp-content/uploads/2015/04/Deluge-No-module-named-gobject-error-450x105.png 450w, /wp-content/uploads/2015/04/Deluge-No-module-named-gobject-error.png 734w" sizes="(max-width: 450px) 100vw, 450px" /><figcaption id="caption-attachment-3540" class="wp-caption-text">No module named gobject</figcaption></figure>

I just installed Deluge on Archlinux but the GUI kept failing to come up with  &#8220;No module named gobject&#8221;.

This happens because installing just the deluge package does not meet all the dependencies required to run the GUI. Install &#8220;python-gobject2&#8221; and &#8220;pygtk&#8221; packages to satisfy the dependencies and Deluge will run fine.

`$pacman -Sy python-gobject2 pygtk`