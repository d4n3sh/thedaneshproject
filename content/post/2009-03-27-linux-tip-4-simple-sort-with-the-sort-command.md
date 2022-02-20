---
title: 'Linux Tip #4: Simple sort with the sort command'
author: Danesh
date: 2009-03-27T08:41:02+00:00
url: /posts/linux-tip-4-simple-sort-with-the-sort-command/
robotsmeta:
  - index,follow
pvc_views:
  - 3279
dsq_thread_id:
  - 897358349

---
You can easily sort your outputs in Linux using the &#8220;sort&#8221; command. Simply pipe &#8220;|&#8221; your output to a &#8220;sort&#8221; command and you should see the sorted results.

See sample usage below. This is just to start off, I&#8217;ve cover more in future posts.

`[root@hantu ~]# cat numbers<br />
5<br />
4<br />
3<br />
2<br />
1<br />
0<br />
6<br />
7<br />
8<br />
9`

`[root@hantu ~]# cat numbers | sort<br />
0<br />
1<br />
2<br />
3<br />
4<br />
5<br />
6<br />
7<br />
8<br />
9`

`[root@hantu ~]# cat numbers | sort -r<br />
9<br />
8<br />
7<br />
6<br />
5<br />
4<br />
3<br />
2<br />
1<br />
0`

Happy sorting!!