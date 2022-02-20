---
title: How to set default session timeout in Linux
author: Danesh
date: 2008-03-05T04:44:19+00:00
url: /posts/how-to-set-default-session-timeout-in-linux/
pvc_views:
  - 60179
dsq_thread_id:
  - 889769065

---
My DC operation guys access Linux servers on a daily basis but somehow they never remember to log out. This is a security risk as anyone could gain access to the open console and create caos.

Today, yet again I&#8217;m forced to play the bad guy by dummy proofing my Linux servers by implementing default timeout for user sessions.

Bash and Korn both support the TMOUT variable which I will use to set the default timeout.

The etc/.bashrc file will apply the timeout system wide but if you need it to be user specific then modify the ~/.bashrc file instead.

Here&#8217;s how it&#8217;s done.

    echo "TMOUT=300 >> /etc/bashrc

    echo "readonly TMOUT" >> /etc/bashrc

    echo "export TMOUT" >> /etc/bashrc

Log off, start a new session and wait for 5 minutes. Your session should terminate