---
title: Spotify won’t play local files on Linux
author: Danesh
date: 2014-03-10T16:19:17+00:00
url: /posts/spotify-wont-play-local-files-linux/
dsq_thread_id:
  - 2401860040

---
<a href="/posts/install-spotify-client-arch-linux/spotify-logo-primary-horizontal-light-background-rgb-450x175/" rel="attachment wp-att-3411"><img loading="lazy" class="alignnone size-full wp-image-3411" alt="spotify-logo-primary-horizontal-light-background-rgb-450x175" src="/wp-content/uploads/2014/01/spotify-logo-primary-horizontal-light-background-rgb-450x175.jpg" width="450" height="175" /></a>

I&#8217;m running Spotify version 0.9.4.183-1 and  local mp3 files don&#8217;t play anymore.

All I get from the logs is &#8220;15:58:39.156 I [audio\_driver\_linux.cpp:18 ] Using PulseAudio&#8221;, no proper error message 🙁

After some googling, the fix was simple enough. Install the &#8220;ffmpeg-compat&#8221; package from the office repo.

`sudo pacman -S ffmpeg-compat<br />
`  
Restart spotify and your local mp3 files should now play in your Spotify client.

Source: [ArchWiki][1]

 [1]: https://wiki.archlinux.org/index.php/spotify#Spotify_won.27t_play_local_files