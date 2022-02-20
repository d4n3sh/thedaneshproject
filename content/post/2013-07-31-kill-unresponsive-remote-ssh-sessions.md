---
title: Kill Unresponsive remote SSH Sessions
author: Danesh
date: 2013-07-31T11:13:53+00:00
url: /posts/kill-unresponsive-remote-ssh-sessions/
dsq_thread_id:
  - 1550775904

---
[<img loading="lazy" class="alignnone size-medium wp-image-3271" alt="ssh-escape-cha_2013-07-31_19-11-17" src="/wp-content/uploads/2013/07/ssh-escape-cha_2013-07-31_19-11-17-450x154.png" width="450" height="154" srcset="/wp-content/uploads/2013/07/ssh-escape-cha_2013-07-31_19-11-17-450x154.png 450w, /wp-content/uploads/2013/07/ssh-escape-cha_2013-07-31_19-11-17.png 544w" sizes="(max-width: 450px) 100vw, 450px" />][1]

I spend a lot of time working with ssh terminals over very slow connections. One common  issue that crops up often  is unresponsive terminals. Closing the terminal is what most of us would go with but then you would have to go through the login workflow again.  If you had to login to 3 servers then redoing that every time would be a pain.

Here&#8217;s a quick tip. The next time your ssh session becomes unresponsive, hit &#8220;ENTER&#8221; , followed the  &#8220;~&#8221; key and finally the  &#8220;.&#8221; key. ( **ENTER** , **~** , **.** ) . That will terminate the unresponsive session but still keep you within your main ssh session.

SSH supports a bunch of escape characters. It&#8217;s a less known feature but in my case proved handy. To see a list of all the supported escape characters run &#8221; **ENTER** , **~** , **?** &#8220;.

`[root@server conf.d]# ~?<br />
Supported escape sequences:<br />
~. - terminate connection (and any multiplexed sessions)<br />
~B - send a BREAK to the remote system<br />
~C - open a command line<br />
~R - Request rekey (SSH protocol 2 only)<br />
~^Z - suspend ssh<br />
~# - list forwarded connections<br />
~& - background ssh (when waiting for connections to terminate)<br />
~? - this message<br />
~~ - send the escape character by typing it twice`  
(Note that escapes are only recognized immediately after newline.)

 [1]: /wp-content/uploads/2013/07/ssh-escape-cha_2013-07-31_19-11-17.png