---
title: Installing ps3mediaserver on Fedora 11
author: Danesh
date: 2009-07-06T00:00:36+00:00
aktt_notify_twitter:
  - no
pvc_views:
  - 13461
dsq_thread_id:
  - 891038727

---
Most of my movie and audio files are on my Linux box.  Currently, I use [ps3mediaserver][1] to get all my media across to my PS3 which is my media center. Aaaaa... the simplicity is just amazing.

PS3mediaserver is Java based and getting it set-up is a breeze. Here's how,

1. Download the tar package. Remember to download the most recent version. [Look here][2]

`[danesh@jackal ~]$ wget http://ps3mediaserver.googlecode.com/files/pms-linux-1.10.5.tgz`

2. Extract the download tar package.

`[danesh@jackal ~]$ tar -zxvf pms-linux-1.10.5.tgz`

3. Go in to the new extracted foder and start the server by executing the "PMS.sh" script. Also, remember to give execute rights to the "PMS.sh" script by running chmod +x.

`[danesh@jackal ~]$ chmod +x PMS.sh</p>
<p>[danesh@jackal ~]$ cd pms-linux-1.10.5</p>
<p>[danesh@jackal ~]$ ./PMS.sh`

That's it, turn on your ps3 and start enjoying your new media server.

[<img loading="lazy" class="alignnone size-medium wp-image-1597" title="Screenshot-Java PS3 Media Server v1.10.5" src="/wp-content/uploads/2009/07/Screenshot-Java-PS3-Media-Server-v1.10.5-499x365.png" alt="Screenshot-Java PS3 Media Server v1.10.5" width="499" height="365" srcset="/wp-content/uploads/2009/07/Screenshot-Java-PS3-Media-Server-v1.10.5-499x365.png 499w, /wp-content/uploads/2009/07/Screenshot-Java-PS3-Media-Server-v1.10.5.png 994w" sizes="(max-width: 499px) 100vw, 499px" />][3]

 [1]: http://code.google.com/p/ps3mediaserver/
 [2]: http://code.google.com/p/ps3mediaserver/downloads/list
 [3]: /wp-content/uploads/2009/07/Screenshot-Java-PS3-Media-Server-v1.10.5.png