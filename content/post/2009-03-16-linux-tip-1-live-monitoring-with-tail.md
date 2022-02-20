---
title: 'Linux Tip #1: Live monitoring with tail'
author: Danesh
date: 2009-03-16T04:40:17+00:00
url: /posts/linux-tip-1-live-monitoring-with-tail/
robotsmeta:
  - index,follow
pvc_views:
  - 2045
dsq_thread_id:
  - 891432868

---
This is something every Linux admin or Linux superuser probably already knows and uses everyday.

The &#8220;tail -f&#8221; command monitors a file and tracks any changes to it. As changes are made to the monitored file the &#8220;tail&#8221; command will print them on screen. Live monitoring basically&#8230;..

`tail -f [log file]`

Sample output;

`[root@keke ~]# tail -f /var/log/messages</p>
<p>Mar 16 11:06:39 keke dhcpd: DHCPREQUEST for 172.28.6.233 from 00:1b:78:d2:bc:0e via eth0<br />
Mar 16 11:06:39 keke dhcpd: DHCPACK on 172.28.6.233 to 00:1b:78:d2:bc:0e via eth0<br />
Mar 16 11:06:39 abubu dhclient: DHCPREQUEST on eth0 to 172.28.1.41 port 67<br />
Mar 16 11:06:39 abubu dhclient: DHCPACK from 172.28.1.41<br />
Mar 16 11:06:39 abubu dhclient: bound to 172.28.6.233 -- renewal in 33912 seconds.<br />
Mar 16 11:06:46 keke dhcpd: DHCPDISCOVER from 00:14:5e:ce:66:14 via eth0<br />
Mar 16 11:06:46 keke dhcpd: DHCPOFFER on 172.28.4.123 to 00:14:5e:ce:66:14 via eth0<br />
Mar 16 11:06:54 keke dhcpd: DHCPREQUEST for 172.28.4.123 (172.28.1.41) from 00:14:5e:ce:66:14 via eth0<br />
Mar 16 11:06:54 keke dhcpd: DHCPACK on 172.28.4.123 to 00:14:5e:ce:66:14 via eth0<br />
Mar 16 11:06:54 keke atftpd[21175]: Serving /tftpboot/pxelinux.0 to 172.28.4.123:2070<br />
Mar 16 11:06:54 keke atftpd[21175]: Serving /tftpboot/pxelinux.0 to 172.28.4.123:2071<br />
Mar 16 11:06:54 keke atftpd[21175]: Serving /tftpboot/pxelinux.cfg/01-00-14-5e-ce-66-14 to 172.28.4.123:57089<br />
Mar 16 11:06:54 keke atftpd[21175]: Serving /tftpboot/pxelinux.cfg/AC1C047B to 172.28.4.123:57090`