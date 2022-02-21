---
title: How to change your MikroTik router’s name
author: Danesh
date: 2015-08-15T02:11:37+00:00
dsq_thread_id:
  - 4034066041

---
Via Web or WinBox

System > Identity

<figure id="attachment_3565" aria-describedby="caption-attachment-3565" style="width: 450px" class="wp-caption alignnone"><img loading="lazy" class="size-medium wp-image-3565" src="/wp-content/uploads/2015/08/mikrotik-change-hostsname-winbox-450x254.png" alt="Change MikroTik Hostname via WinBox" width="450" height="254" srcset="/wp-content/uploads/2015/08/mikrotik-change-hostsname-winbox-450x254.png 450w, /wp-content/uploads/2015/08/mikrotik-change-hostsname-winbox.png 466w" sizes="(max-width: 450px) 100vw, 450px" /><figcaption id="caption-attachment-3565" class="wp-caption-text">Change MikroTik Hostname via WinBox</figcaption></figure>

If you prefer the Terminal

[admin@oldname] > system identity print  
[admin@oldname] > system identity set name=newname  
[admin@oldname] > system identity print

<figure id="attachment_3564" aria-describedby="caption-attachment-3564" style="width: 448px" class="wp-caption alignnone"><img loading="lazy" class="size-full wp-image-3564" src="/wp-content/uploads/2015/08/mikrotik-change-hostsname.png" alt="Change MikroTik Hostname" width="448" height="99" /><figcaption id="caption-attachment-3564" class="wp-caption-text">Change MikroTik Hostname</figcaption></figure>