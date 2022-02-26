---
title: Enable Medibuntu in Ubuntu 8.10
author: Danesh Manoharan
date: 2008-11-25T06:37:13+00:00
pvc_views:
  - 11822
robotsmeta:
  - index,follow
aktt_notify_twitter:
  - no
dsq_thread_id:
  - 895984348

---
[Medibuntu][1] if you don't already know is the Ubuntu repository for [non-free][2] [packages][3] which can't be bundled with Ubuntu for regal reasons. Acrobat reader, quick time player, windows specific video/audio codecs, DVD support and the list goes on.

Adding the Medibuntu repository into your Ubuntu 8.10 is easy.

1. Fire up your terminal and run,

```
sudo wget http://www.medibuntu.org/sources.list.d/intrepid.list --output-document=/etc/apt/sources.list.d/medibuntu.list
```

2. Install the GPG keys. While still in the terminal run,

```
sudo apt-get update && sudo apt-get install medibuntu-keyring && sudo apt-get update
```

3. Install support for Windows codecs.

sudo apt-get install w32codecs

Sources: [Medibuntu][2] | [Launchpad][4]

 [1]: http://www.medibuntu.org/
 [2]: https://help.ubuntu.com/community/Medibuntu
 [3]: http://packages.medibuntu.org/
 [4]: https://launchpad.net/medibuntu/