---
title: How to run IE in openSUSE 10.3
author: Danesh
date: 2008-02-23T19:08:29+00:00
pvc_views:
  - 16391
dsq_thread_id:
  - 890153260

---
You decided to switch desktops to Linux and now you can't access your office IE only intranet. What do you do?

Well, you could IEs4Linux on WINE. [WINE][1] is a opensource Windows API implementation for the Linux platform and [IEs4Linux][2] is the "installer" which will download, install and get IE to work with WINE.

1. Add the WINE repository for openSUSE 10.3.

YaST2 -> Software -> Software Repositories.

http://software.opensuse.org/download/Emulators:/Wine/openSUSE_10.3/

[![][3]][4]

<!--more-->2. Install the WINE and cabextract package.

YaST2 -> Software -> Software Management.

[![][5]][6]

3. Download IEs4Linux from [here][7] or use the command line method shown below.

 ``

<pre>wget http://www.tatanka.com.br/ies4linux/downloads/ies4linux-latest.tar.gz</pre>

4. Extract and run the IEs4Linux installer. You don't need to be root for this.

 ``

<pre>tar zxvf ies4linux-latest.tar.gz
cd ies4linux-*
./ies4linux</pre>

[![][8]][9] [![][10]][11] [![][12]][13] [![][14]][15]  
[![][16]][16] [![][17]][18]

That's it, enjoy your IE in Linux but note the there is no support for streaming video, currently only flash is supported.

[![][17]][18]

Once you're bored (like I did) then it's time to get rid of IE, here's how you'll do that since there is no uninstaller for IEs4Linux.

 ``

<pre>danny@pandora:~&gt; rm -rf ~/.ies4linux/
danny@pandora:~&gt; rm -rf ~/bin/
danny@pandora:~&gt; rm -rf ~/Desktop/ies4linux-ie6.desktop</pre>

 [1]: http://www.winehq.org/
 [2]: http://www.tatanka.com.br/ies4linux/page/Main_Page
 [3]: http://img110.imageshack.us/img110/6796/wine1od2.th.jpg
 [4]: http://img110.imageshack.us/img110/6796/wine1od2.jpg
 [5]: http://img239.imageshack.us/img239/5200/wine2ju5.th.jpg
 [6]: http://img239.imageshack.us/img239/5200/wine2ju5.jpg
 [7]: http://www.tatanka.com.br/ies4linux/download.html
 [8]: http://img89.imageshack.us/img89/8959/wine5ac8.th.jpg
 [9]: http://img89.imageshack.us/img89/8959/wine5ac8.jpg
 [10]: http://img100.imageshack.us/img100/4672/wine6hz1.th.jpg
 [11]: http://img100.imageshack.us/img100/4672/wine6hz1.jpg
 [12]: http://img141.imageshack.us/img141/3478/wine11hl1.th.jpg
 [13]: http://img141.imageshack.us/img141/3478/wine11hl1.jpg
 [14]: http://img144.imageshack.us/img144/4225/wine16mm0.th.jpg
 [15]: http://img144.imageshack.us/img144/4225/wine16mm0.jpg
 [16]: http://img149.imageshack.us/img149/7667/wine17uq5.jpg
 [17]: http://img150.imageshack.us/img150/3893/wine18lf1.th.jpg
 [18]: http://img150.imageshack.us/img150/3893/wine18lf1.jpg