---
title: Firefox 3 beats IE7 in memory consumption
author: Danesh
date: 2008-03-19T12:26:57+00:00
url: /posts/firefox-3-beats-ie7-in-memory-consumption/
pvc_views:
  - 3424
dsq_thread_id:
  - 980544989

---
[<img border="0" src="http://static.flickr.com/2379/2345397694_c6c319bef1_m.jpg" alt="Firefox bites IE" />][1]

Firefox 3 Beta 4 is out and it&#8217;s beating Microsoft&#8217;s IE7 in the memory consumption arena.

As browsers improve so do their hunger for memory but to what limit is the question. The competition will eventually boil down to which browser uses the least amount of memory to accomplish the general requirements of a browser. Currently Firefox 3 has managed to beat Firefox 2 and IE7 by working around the 100MB mark after loading and unloading 30 random web pages. The graph below will speak for itself, at peak (30 pages) IE7 was consuming around 500MB while Firefox 2 hovered around 280MB and Firefox 3 steadily working around 200MB. [<img border="0" src="http://static.flickr.com/2130/2344570169_1db87c2cd2.jpg" alt="Firefox memory consumption graph" />][2]

IE8 is said to attention the memory issue but till then it&#8217;s looks like the road is clear for Firefox 3.

If you are interested in running the benchmark, there&#8217;s a python script which will load open and load 30 random pages for you. Run the benchmark [here][3] or download the [script][4].

[Download Firefox 3 Beta 4][5]

Source: [Paulou.net][6] [ Stuart Parmenter (Mozilla Developer) ]

 [1]: http://www.flickr.com/photos/65059925@N00/2345397694/ "Firefox bites IE"
 [2]: http://www.flickr.com/photos/65059925@N00/2344570169/ "Firefox memory consumption graph"
 [3]: http://random.pavlov.net/membuster/index.html
 [4]: http://random.pavlov.net/membuster/measure2.py
 [5]: http://www.mozilla.com/en-US/firefox/all-beta.html
 [6]: http://blog.pavlov.net/2008/03/11/firefox-3-memory-usage/