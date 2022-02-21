---
title: How to install Microsoft Core Fonts on Linux
author: Danesh
date: 2008-02-26T12:58:36+00:00
pvc_views:
  - 22439
dsq_thread_id:
  - 889986327

---
![][1]

Most Linux desktop users don&#8217;t fancy the default fonts which ship default with Linux. Luckily there are a few ways you could easy enjoy Microsoft fonts on your Linux desktop.

The simplest way would be to use the package manager to add distro specific packages to install the fonts. openSUSE, Ubuntu and many other distros now provide the fonts with a disclaimer which you will have to agree to before the fonts get installed.

If the above did not work for you then download this rpm package: ftp://ftp.gwdg.de/pub/linux/misc/suser-jengelh/AnyDistro/noarch/MicrosoftFonts-1-jen14.noarch.rpm which will provide the fonts for you. Use your package manager to install the package or simply install it from the command line using the command below. An advantage of this rpm package is that it includes the Tahoma fonts which is not included by the distro specific packages.

    rpm -ivh  MicrosoftFonts-1-jen14.noarch.rpm

The third and final way which is also the legal way would be to copy the fonts over from a licensed Windows XP computer. Move them over using winscp or a usb thumb drive,WinSCP in my case. Once moved over simply use your font&#8217; manager to install them. In my case KDE, the font manger can be accessed at KDE Menu -> Configure Desktop -> System Administration -> Font Installer -> &#8220;Administrator Mode&#8221;.

Enjoy your fonts, drop me a comment if you need help.

 [1]: http://img299.imageshack.us/img299/1475/mscorefontsmy9.jpg