---
title: support.microsoft.com not working behind Squid
author: Danesh
date: 2008-04-25T23:34:08+00:00
pvc_views:
  - 19641
dsq_thread_id:
  - 891038746

---
Can you access support.microsoft.com? Chances are you can&#8217;t if you&#8217;re behind a squid proxy.

Here&#8217;s the fix/workaround,

Add the lines below into your squid.conf file. should be in /etc/squid/squid.conf. Restart squid and you should be good to go.

#> vi /etc/squid/squid.conf

add lines into /etc/squid.conf  
\# Fix support.microsoft.com by removing Accept-Encoding header  
acl support.microsoft.com dstdomain support.microsoft.com  
header_access Accept-Encoding deny support.microsoft.com

#> service squid restart

The other way is to remove the tick from &#8220;Use HTTP1.1 through proxy connections&#8221; in IE&#8217;s Advanced internet options tab. Beware that this might break other sites.

Source: [Whirlpool.net.au][1]

Update:

Newer versions of squid need a different approach as demonstrated by Dave over at [davehope.co.uk][2]

 [1]: http://forums.whirlpool.net.au/forum-replies-archive.cfm/959960.html
 [2]: http://davehope.co.uk/Blog/microsoft-break-supportmicrosoftcom-for-squid-users/#comment-582