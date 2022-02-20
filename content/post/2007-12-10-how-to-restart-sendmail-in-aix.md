---
title: How to restart sendmail in AIX
author: Danesh
date: 2007-12-10T15:29:21+00:00
url: /posts/how-to-restart-sendmail-in-aix/
pvc_views:
  - 37643
dsq_thread_id:
  - 889737807

---
I had to work with an AIX box today which was having some issues with the mailq getting filled up frequently. The issue was not with the AIX box but the out SMTP box. Damn those spammers!!

Anyway, I had to restart the sendmail daemon on the AIX box. Walk through below,

1. Verify if sendmail is running. &#8220;_**ps -ef | grep sendmail**_&#8220;.

This should show: <span id="intelliTxt">root 5704 1 0 11:08:42 &#8211; 0:00 sendmail: accepting connections on port 25</span>

2. Stop sendmail. &#8220;_**stopsrc -s sendmail**_&#8221; or &#8220;_**kill -1 \`cat /etc/senamail.pid**_\`.

3. Verify if sendmail is running. &#8220;_**ps -ef | grep sendmail**_&#8220;.

No process should be returned.

4. Start sendmail. &#8220;_**startsrc -s sendmail -a &#8220;-bd -q30m&#8221;**_&#8220;.

-bd will start the sendmail as a SMTP mail relay router.

-q will the the interval in which the sendmail daemon will process save messages. If none is provided the daemon will default to instant processing.

5. Verify if sendmail is running. &#8220;_**ps -ef | grep sendmail**_&#8220;.

This should show: <span id="intelliTxt">root 5704 1 0 11:30:23 &#8211; 0:00 sendmail: accepting connections on port 25</span>