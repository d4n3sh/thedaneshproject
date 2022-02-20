---
title: How to enable presto in Fedora 11
author: Danesh
date: 2009-08-21T23:00:55+00:00
url: /posts/how-to-enable-presto-in-fedora-11/
aktt_notify_twitter:
  - no
pvc_views:
  - 3481
dsq_thread_id:
  - 890529262

---
Delta RPMs is a bandwidth saver. Instead of downloading full rpm files on updates, delta rpms (.drpm) hold only the changes in binary form. The size of the packages is now significantly reduced thus saving bandwidth. Once downloaded the drpm file get reconstructed to form the full package before they gets applied. On avg I see 70% bandwidth savings after moving to Presto.

[Presto][1] is the Fedora project to enable delta rpms on all Fedora repositories. Fedora 11 is Presto enabled.

I&#8217;ll walk you through setting presto up.

1. Search your repos to make sure the yum-presto package is available.

`[root@bamboo]# yum search yum-presto`

2. Install the yum-presto package.

`[root@bamboo]# yum install yum-presto`

3. Try running an update to see presto in action.

`[root@bamboo]# yum -y update<br />
....................<br />
....................<br />
....................<br />
Finishing rebuild of rpms, from deltarpms<br />
<delta rebuild>                                                           |  79 MB     01:14<br />
Presto reduced the updates to 33 M from 79 M which is a 59% savings.`

 [1]: http://fedoraproject.org/wiki/Releases/FeaturePresto