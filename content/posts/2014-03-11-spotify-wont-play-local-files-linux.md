---
title: Spotify won’t play local files on Linux
author: Danesh Manoharan
date: 2014-03-10T16:19:17+00:00
---
[![spotify-logo-primary-horizontal-light-background-rgb-450x175](/wp-content/uploads/2014/01/spotify-logo-primary-horizontal-light-background-rgb-450x175.jpg)](/posts/install-spotify-client-arch-linux/spotify-logo-primary-horizontal-light-background-rgb-450x175/)

I'm running Spotify version 0.9.4.183-1 and  local mp3 files don't play anymore.

All I get from the logs is "15:58:39.156 I [audio\_driver\_linux.cpp:18 ] Using PulseAudio", no proper error message 🙁

After some googling, the fix was simple enough. Install the "ffmpeg-compat" package from the office repo.

`sudo pacman -S ffmpeg-compat`

Restart spotify and your local mp3 files should now play in your Spotify client.

Source: [ArchWiki][1]

[1]: https://wiki.archlinux.org/index.php/spotify#Spotify_won.27t_play_local_files
