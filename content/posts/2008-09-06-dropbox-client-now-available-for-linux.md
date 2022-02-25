---
title: Dropbox client now available for Linux
author: Danesh Manoharan
date: 2008-09-06T05:51:18+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 12089
dsq_thread_id:
  - 889726622

---
[<img loading="lazy" class="alignnone size-medium wp-image-878" title="dropbox-asci" src="/wp-content/uploads/2008/09/dropbox-asci.png" alt="" width="291" height="89" />][1]

[][1]The folks at [dropbox][2]Ã‚Â released the much anticipated Linux client yesterday. Currently it's designed as a nautilus extension. Support for Konqueror should be available soon.

The nautilus extension is opensource but the dropboxd daemon which keeps the files in sync is closedÃ‚Â source.

Packages for Ubuntu and Fedora are available for download. For other distros you'll need to compile from source. Go to the download page.Ã‚Â 

I managed to get dropbox working on my openSUSE 11 running KDE. It's quite simple actually. You need to install the nautilus and nautilus-devel pakages before compiling the source,

1. install nautilus

`root#> zypper in nautilus<br />
`  
2. install nautilus-devel

`root#>Ã‚Â zypper in nautilus-devel<br />
`  
3. compile the dropbox source. Make sure to be in the source folder first.

`root#>Ã‚Â ./configure<br />
`  
`root#>Ã‚Â make<br />
`  
`root#>Ã‚Â make install<br />
`  
4. start nautilus or the dropboxd daemon to initiate the dropbox client.Ã‚Â 

`root#>Ã‚Â nautilus<br />
`  
or

`root#> cd /home/[user]/.dropbox-dist/<br />
`  
`root#> ./dropboxd`

 [1]: /wp-content/uploads/2008/09/dropbox-asci.png
 [2]: http://getdropbox.com