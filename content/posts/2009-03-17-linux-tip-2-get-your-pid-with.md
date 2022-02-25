---
title: 'Linux Tip #2: Get your PID with $$'
author: Danesh Manoharan
date: 2009-03-17T02:00:11+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 2764
dsq_thread_id:
  - 921939366

---
"$$" is a useful Linux variable you could use in your script to get it's PID. The "$$" variable always holds the PID of the executing process. 

Why do you need it? Maybe to check if the script is already running? This is what I normally use it for.

Sample Script;

`#!/bin/bash<br />
echo "My PID is $$"<br />
sleep 2`

Sample Output;

`[root@keke ~]# ./test1.sh<br />
My PID is 8909`