---
title: How to find your Ubuntu version
author: Danesh
date: 2008-09-21T04:34:41+00:00
url: /posts/how-to-find-your-ubuntu-version/
robotsmeta:
  - index,follow
pvc_views:
  - 3486
dsq_thread_id:
  - 946400321

---
2 easy ways find out what version of Ubuntu you&#8217;re running.

**First option,**

cat the /etc/issue file.

`danny@family-desktop:/etc$ cat /etc/issue<br />
Ubuntu 8.04.1 \n \l`

**Second option**

cat the /etc/lsb-release file.

`danny@family-desktop:/etc$ cat /etc/lsb-release<br />
DISTRIB_ID=Ubuntu<br />
DISTRIB_RELEASE=8.04<br />
DISTRIB_CODENAME=hardy<br />
DISTRIB_DESCRIPTION="Ubuntu 8.04.1"`

or

run the lsb_release command with the &#8220;-a&#8221; switch.

`danny@family-desktop:/etc$ lsb_release -a<br />
No LSB modules are available.<br />
Distributor ID: Ubuntu<br />
Description:Ã‚Â Ã‚Â Ã‚Â  Ubuntu 8.04.1<br />
Release:Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  8.04<br />
Codename:Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  hardy`