---
title: 'N: Skipping acquire of configured file ‘contrib/binary-i386/Packages’ as repository ‘https://download.virtualbox.org/virtualbox/debian bionic InRelease’ doesn’t support architecture ‘i386’'
author: Danesh
date: 2018-08-15T05:07:51+00:00

---
N: Skipping acquire of configured file 'contrib/binary-i386/Packages' as repository 'https://download.virtualbox.org/virtualbox/debian bionic InRelease' doesn't support architecture 'i386'

There's no 32bit support now so update the source list file to get rid of the warning.

In my case, /etc/apt/sources.list.d/virtualbox.list

Change

<pre class="toolbar:2 nums:false lang:default decode:true">deb https://download.virtualbox.org/virtualbox/debian bionic contrib</pre>

to

<pre class="toolbar:2 nums:false lang:default decode:true">deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian bionic contrib</pre>

&nbsp;