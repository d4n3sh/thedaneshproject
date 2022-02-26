---
title: How to Install Spotify client on Arch Linux
author: Danesh Manoharan
date: 2014-01-09T14:40:54+00:00
---
![](/wp-content/uploads/2014/01/spotify-logo-primary-horizontal-light-background-rgb-450x175.jpg)

The Spotify client is available through WINE or natively through the AUR. I'll walk you through the AUR way.

1. Download the Spotify package from the AUR. [[Spotify AUR][1]]

`wget https://aur.archlinux.org/packages/sp/spotify/spotify.tar.gz`

2. Unpack the package and compile.

```
tar -zxvf spotify.tar.gz</p>
cd spotify/
makepkg -s
` `` 
The "-s" switch will use pacman to resolve any dependencies.

3. Install the compile package.

`pacman -U spotify-0.9.4.183-2-x86_64.pkg.tar.xz`

 [1]: https://aur.archlinux.org/packages/spotify/
