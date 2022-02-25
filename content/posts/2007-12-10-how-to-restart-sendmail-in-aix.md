---
title: How to restart sendmail in AIX
author: Danesh Manoharan
date: 2007-12-10T15:29:21+00:00
pvc_views:
  - 37643
dsq_thread_id:
  - 889737807

---
I had to work with an AIX box today which was having some issues with the mailq getting filled up frequently. The issue was not with the AIX box but the out SMTP box. Damn those spammers!!

Anyway, I had to restart the sendmail daemon on the AIX box. Walk through below,

1. Verify if sendmail is running. "_**ps -ef | grep sendmail**_".

This should show: <span id="intelliTxt">root 5704 1 0 11:08:42 - 0:00 sendmail: accepting connections on port 25</span>

2. Stop sendmail. "_**stopsrc -s sendmail**_" or "_**kill -1 \`cat /etc/senamail.pid**_\`.

3. Verify if sendmail is running. "_**ps -ef | grep sendmail**_".

No process should be returned.

4. Start sendmail. "_**startsrc -s sendmail -a "-bd -q30m"**_".

-bd will start the sendmail as a SMTP mail relay router.

-q will the the interval in which the sendmail daemon will process save messages. If none is provided the daemon will default to instant processing.

5. Verify if sendmail is running. "_**ps -ef | grep sendmail**_".

This should show: <span id="intelliTxt">root 5704 1 0 11:30:23 - 0:00 sendmail: accepting connections on port 25</span>