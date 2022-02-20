---
title: 'N: Skipping acquire of configured file ‘contrib/binary-i386/Packages’ as repository ‘https://download.virtualbox.org/virtualbox/debian bionic InRelease’ doesn’t support architecture ‘i386’'
author: Danesh
date: 2018-08-15T05:07:51+00:00
url: /posts/n-skipping-acquire-of-configured-file-contrib-binary-i386-packages-as-repository-https-download-virtualbox-org-virtualbox-debian-bionic-inrelease-doesnt-support-architecture-i386/

---
N: Skipping acquire of configured file &#8216;contrib/binary-i386/Packages&#8217; as repository &#8216;https://download.virtualbox.org/virtualbox/debian bionic InRelease&#8217; doesn&#8217;t support architecture &#8216;i386&#8217;

There&#8217;s no 32bit support now so update the source list file to get rid of the warning.

In my case, /etc/apt/sources.list.d/virtualbox.list

Change

<pre class="toolbar:2 nums:false lang:default decode:true">deb https://download.virtualbox.org/virtualbox/debian bionic contrib</pre>

to

<pre class="toolbar:2 nums:false lang:default decode:true">deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian bionic contrib</pre>

&nbsp;