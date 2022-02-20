---
title: Extract rar files in Linux
author: Danesh
date: 2007-08-15T01:33:32+00:00
url: /posts/extract-rar-files-in-linux/
pvc_views:
  - 75074
dsq_thread_id:
  - 889737739

---
RAR is a proprietary compression format widely used today. It&#8217;s supposedly has 30% higher compression rate when compared with [WinZip][1]. If you download large torrent then chances are you are are already well acquainted with RAR.

I use RAR on my Windows and Linux boxes everyday and today I&#8217;ll show you how to extract RAR files from the Linux command line.

In Linux, to extract a RAR file you would use the unrar command. The unrar binaries are typically not included with the default Linux install so you will have to install them either through the package manager or by downloading binaries from rarlab.com

Let&#8217;s get to the HowTo now,

Extract a RAR file into the curren directory.

> \# unrar e [filename].rar

Extract a RAR file with the full file path.

> \# unrar x [filename].rar

List contents of a RAR file

> \# unrar l [filename].rar

Test intergruty of a RAR file

> \# unrar t [filename].rar

If you face any problems obtaining,installing or using unrar please contact me. I will be glad to help.

 [1]: http://www.winzip.com/index.htm