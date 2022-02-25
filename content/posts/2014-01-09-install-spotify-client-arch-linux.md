---
title: How to Install Spotify client on Arch Linux
author: Danesh Manoharan
date: 2014-01-09T14:40:54+00:00
dsq_thread_id:
  - 2102524860

---
<a href="/posts/install-spotify-client-arch-linux/spotify-logo-primary-horizontal-light-background-rgb-450x175/" rel="attachment wp-att-3411"><img loading="lazy" class="alignnone size-full wp-image-3411" alt="spotify-logo-primary-horizontal-light-background-rgb-450x175" src="/wp-content/uploads/2014/01/spotify-logo-primary-horizontal-light-background-rgb-450x175.jpg" width="450" height="175" /></a>

The Spotify client is available through WINE or natively through the AUR. I'll walk you through the AUR way.

1. Download the Spotify package from the AUR. [[Spotify AUR][1]]

`wget https://aur.archlinux.org/packages/sp/spotify/spotify.tar.gz<br />
`  
2. Unpack the package and compile.

`<br />
tar -zxvf spotify.tar.gz</p>
<p>cd spotify/</p>
<p>makepkg -s<br />
`  
The "-s" switch will use pacman to resolve any dependencies.

3. Install the compile package.

`pacman -U spotify-0.9.4.183-2-x86_64.pkg.tar.xz`

 [1]: https://aur.archlinux.org/packages/spotify/