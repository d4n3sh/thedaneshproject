---
title: Deluge BitTorrent Client
author: Danesh
date: 2007-08-08T09:02:16+00:00
pvc_views:
  - 4380
dsq_thread_id:
  - 889736918

---
I was talking to [Wing Loon][1] a few days back about how to bypass all the bandwidth throttling being enforced by our magnificent ISPs here. He recommended to try [Deluge][2] as he heard that it managed to bypass the bandwidth throttling.

I decided to try it out last night on my openSUSE 10.2 desktop. Install was pretty simple as the rpm was made available through YaST2 by adding the [Guru source][3]. Configured some ports to be forwarded though my [IPCop][4] and finally added torrents from [releaselog][5] and [thepiratebay][6], my 2 favorite torrent sites.

Immediately, I saw a miracle unfold in front of me, something I thought I would never see again since moving back from PenangFon to Streamyx when I moved back to KL. I was getting 100kB ++ download speeds. At first, I did not believe it, so I cross checked by looking at my network utilization through IPCop and truly enough it was also showing speeds in access of 100kB.(See screenshot below to believe). Well, I know 100kB ain't much when compared to what other ISP's provide in other countries but for now 100kB is a luxury here.

Woo Wee!!! My torrenting mood is back on now.....!!

![deluge.jpg][7] 

Deluge is currently Linux only but ports might be coming out soon.

[Get Deluge BitTorrent Client][8] (0.5.4 is the latest stable release at the time of this post. )

[Deluge BitTorrent Client Home][2]

 [1]: http://wingloon.com/2007/08/07/deluge-054/
 [2]: http://deluge-torrent.org/
 [3]: http://ftp.gwdg.de/pub/linux/misc/suser-guru/rpm/10.2/
 [4]: http://www.ipcop.org/
 [5]: http://rlslog.net/
 [6]: http://thepiratebay.org/
 [7]: /wp-content/uploads/2007/08/deluge.jpg
 [8]: http://deluge-torrent.org/downloads