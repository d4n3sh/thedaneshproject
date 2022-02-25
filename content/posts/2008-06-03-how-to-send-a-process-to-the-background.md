---
title: How to send a process to the background
author: Danesh
date: 2008-06-03T07:23:13+00:00
pvc_views:
  - 35357
dsq_thread_id:
  - 889817577

---
Sending a process to the background in Linux is quite easy. All you need is bg, fg, &, and ctrl+Z ( ^Z ).

For this example I will use a simple bash script test.sh I put together to print "Test" every 5 seconds.

``#!/bin/bash<br />
#This script will print "Test" every 5 seconds<br />
#<br />
while [ true ]<br />
do<br />
echo "Test at `date`"<br />
sleep 5<br />
done<br />
#End``

Now let's see how it's done.

`[user@abubu root]$./test.sh &`  
This starts test.sh and sends it to the background. You will be back at shell but should see the "Test" message every 5 seconds.

`[user@abubu root]$jobs<br />
[1]+  Running                 ./test.sh &`  
The jobs command will print all the background processes. Each process is represented by a number to it's left. For example, tesh.sh is represented by 1.

`[user@abubu root]$fg 1`  
The fg command will send the test.sh process to the foreground and return control to the shell.

`[user@abubu root]$ ./test.sh (hit ctrl+Z (^Z) now)<br />
Test at Tue Jun  3 15:11:38 MYT 2008<br />
[1]+  Stopped                 ./test.sh`  
The test.sh process is temporarily suspended.

`[user@abubu root]$bg 1`  
The bg command will send test.sh to the background.

`[user@abubu root]jobs<br />
[1]+  Running                 ./test.sh &`  
The jobs command will print all the background processes. Each process will be represented by a number to it's left. tesh.sh is represented by 1.

`[user@abubu root]$fg 1`  
The fg command will send the test.sh process to the foreground and return control to the shell.

That's it.