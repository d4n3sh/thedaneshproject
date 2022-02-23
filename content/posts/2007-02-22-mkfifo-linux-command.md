---
title: mkfifo | Linux Command
author: Danesh
date: 2007-02-22T08:18:38+00:00
pvc_views:
  - 9089
dsq_thread_id:
  - 889730585

---
_**A short introdution to name pipes as I see them.**_

In the Linux world name pipes are typically used to permit communications between 2 unrelated processes. Name pipes are also known as FIFOs (first in, first out), normally used to establish a one-way flow of data.(half-duplex). Name pipes have a path name of a file associated with them, this is how calling process will reference the name pipes.

Name pipes are file system persistent objects. What this means is that name pipes are always available till the time they are explicitly deleted from the file system as they are represented by as standard files on the file-system. As for standard pipes that we religiously use in our day to day Linux life also known as anonymous pipes are process persistent objects meaning that the name pipes are removed as soon as the processes no longer use them.

_**What does mkfifo do**_

mkfifo is used to create a FIFOs(name pipe). _&#8220;mkfifo test-pipe&#8221;_, now we have a name pipe called &#8220;test-pipe&#8221;.

_&#8220;ls > test-pipe&#8221;_, this pipes the output of the _ls_ command into the name pipe &#8220;test-pipe&#8221;.

_&#8220;cat name-pipe | while read line i; do rm -f $i; done&#8221;_ this will delete the files passed. At this point the &#8220;test-pipe&#8221; will be empty. _&#8220;cat test-pipe&#8221;_ will come up blank.

I&#8217;ve added a screen-shots of the above in action on the next page. Check it out.

I&#8217;m not a Linux guru yet, so guys if my information not accurate or if there is a better way to improve my example please feel free to comment.

<!--more-->

[![mkfifo][1]][2]

 [1]: /wp-content/uploads/2007/02/22feb2007-mkfifo.jpg
 [2]: /wp-content/uploads/2007/02/22feb2007-mkfifo.jpg "mkfifo"