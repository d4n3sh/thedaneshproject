---
title: Automount
author: Danesh
date: 2007-08-13T18:02:40+00:00
pvc_views:
  - 6276
dsq_thread_id:
  - 889737872

---
Decided to drop my permanent mounts and go with automount instead. Why? Well I don't access those folders all the time, they are mainly for backup so mounting only when I need them seemed like a better idea.

I modified the /etc/auto.master file and created a new file named /etc/auto.nosebleed. Contents shown below.

> `# auto.master file`
> 
> /mnt/nosebleed /etc/auto.nosebleed &#8211;timeout=60 &#8211;ghost

> `# auto.nosebleed file`
> 
> mp3 -fstype=cifs,rw,noperm,guest ://10.0.0.200/Mp3  
> ebooks -fstype=cifs,rw,noperm,guest ://10.0.0.200/eBooks  
> movies -fstype=cifs,rw,noperm,guest ://10.0.0.200/Movies  
> scratch -fstype=cifs,rw,noperm,guest ://10.0.0.200/Scratch  
> software -fstype=cifs,rw,noperm,guest ://10.0.0.200/Software  
> tv-shows -fstype=cifs,rw,noperm,guest ://10.0.0.200/Tv-Shows  
> videos -fstype=cifs,rw,noperm,guest ://10.0.0.200/Videos

My options,

_**&#8211;timeout=60**_ will set the ideal time for the mount. If there is not activity for 60 seconds the path will be unmounted.

_**&#8211;ghost**_ will enable the user to see the mountable directory without mounting them.