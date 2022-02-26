---
title: More XWilling than meets the eye…
author: Danesh Manoharan
date: 2007-11-15T14:57:46+00:00
pvc_views:
  - 4151
dsq_thread_id:
  - 889736408

---
I was configuring XDMCP for some of my linux boxes today, when I noticed that [gdm][1] only returns the kernel version, and not some useful info like the amount of users & machine load that Solaris does.

<!--more-->Thats when I realised scouring around 

[The Linux XDMCP HOWTO][2] would be a good idea. GDM provides a method of displaying additional text info as part of the replies. This is done by place a shell script that outputs certain info depending on what you script.

The howto contained a link to a [script][3] that gave exactly what I needed.

<pre>#!/bin/sh

#

# $XFree86$
```

<pre># The output of this script is displayed in the chooser window.
```

<pre># (instead of "Willing to manage")

load="`uptime|sed -e 's/^.*load[^0-9]*//'`"

nrusers="`who|cut -c 1-8|sort -u|wc -l|sed 's/^[        ]*//'`"

s=""; [ "$nrusers" != 1 ] && s=s

echo "${nrusers} user${s}, load: ${load}"
```

  1. Just copy the script to <font color="#000000"><strong>/etc/X11/gdm/XWilling</strong></font>
  2. **chmod 755** it
  3. Walla!! Users & Load Averages

In this picture here, you can see the difference between the hosts with the XWilling script and those without.

P.S. Don't let your inner BOFH script something 'funny' for your users 😉

 [1]: http://en.wikipedia.org/wiki/GNOME_Display_Manager
 [2]: http://en.tldp.org/HOWTO/XDMCP-HOWTO/
 [3]: http://www.penguinlovers.net/linux/xwilling.html