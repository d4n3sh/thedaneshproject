---
title: 'Linux Commands: tee'
author: Danesh Manoharan
date: 2008-03-26T10:51:29+00:00
pvc_views:
  - 8187
dsq_thread_id:
  - 889913116

---
Not many people I know use the tee command but I find it quite useful. I tend to use it quite often in my scripts actually.

So what does it do?

The tee command has the ability to take the standard input and redirected it to multiple outputs. For example, the ls command would normally just return file names on your screen but what if you also need to keep a log of those file names in a text file.

Using the tee command you could simply write something like this "_ls * | tee -a output.txt_". The command will return the file names on screen and also append them to the output.txt file. Screenshot below,

![](http://farm3.static.flickr.com/2079/2363788930_ddc1b8b08e.jpg)

A lightly more complex use of the command. I have a file with duplicate entries. Combining the tee command with the uniq and sort commands I am able print the desired output on screen and also dump it into the file output_sorted.txt. Screenshot below,

![](http://farm4.static.flickr.com/3072/2363810812_64802df38b.jpg)

There are way more usages for the tee command but for today I stuck to the basic. I'll try to post more about it in the future.

 [1]: http://www.flickr.com/photos/dannyportal/2363788930/ "tee1 by vwvr9, on Flickr"
 [2]: http://www.flickr.com/photos/dannyportal/2363810812/ "tee3 by vwvr9, on Flickr"