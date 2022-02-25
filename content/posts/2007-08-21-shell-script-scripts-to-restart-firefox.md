---
title: Shell script scripts to restart firefox
author: Danesh Manoharan
date: 2007-08-20T22:30:23+00:00
pvc_views:
  - 9069
dsq_thread_id:
  - 889737502

---
My Firefox freezes up when I have too many flash videos loading at the same time. Wrote a simple script to restart Firefox every time this happens.

> `#!/bin/bash`  
>  `#simple script to kill and restart firefox`  
>  `#20th August 2007`  
>  `#Writen by Danesh aka Danny`  
>  `#`  
>  `#```  
>  `#look for the firefox PID`  
> `` PID=`ps -ef | grep firefox-bin | grep -v grep | awk Ã¢â‚¬Ëœ{print $2}Ã¢â‚¬â„¢` ``  
>  `#locate firefox executable`  
> `` FIRE=`which firefox` ``  
>  `#kill firefox`  
> `CMD=Ã¢â‚¬?kill -9 $PIDÃ¢â‚¬?`  
>  `` `$CMD` ``  
>  `#pause for 2 seconds`  
>  `` `sleep 2` ``  
>  `#start firefox`  
> `CMD=Ã¢â‚¬?$FIREÃ¢â‚¬?`  
> `` `$CMD &` ``  
>  `#End of script`

I will be adding more functionality to the script in the future. Once sure feature will be the ability to choose either to kill all running instances or just kill a specific instance.