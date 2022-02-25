---
title: 'Linux Tip #4: Simple sort with the sort command'
author: Danesh
date: 2009-03-27T08:41:02+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 3279
dsq_thread_id:
  - 897358349

---
You can easily sort your outputs in Linux using the "sort" command. Simply pipe "|" your output to a "sort" command and you should see the sorted results.

See sample usage below. This is just to start off, I've cover more in future posts.

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