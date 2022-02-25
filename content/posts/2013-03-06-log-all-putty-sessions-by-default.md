---
title: Log all Putty sessions by default
author: Danesh
date: 2013-03-05T22:59:25+00:00
dsq_thread_id:
  - 1120051936

---
Putty has a feature to log your sessions to log files. This is a handy and I use it a lot. Comes in handy when you want to roll back what you did or to simply remember a command you ran.

Session logging is not enabled by default but if you want logging enabled by default for all your sessions then here's how.

Fire up Putty and go to the "Logging" tab. Check "Printable output" option and insert your desired log file name and location into the location field.

[<img loading="lazy" class="alignnone size-medium wp-image-3136" alt="PuTTY Configuration_2013-03-05_22-52-01" src="/wp-content/uploads/2013/03/PuTTY-Configuration_2013-03-05_22-52-01-450x432.png" width="450" height="432" srcset="/wp-content/uploads/2013/03/PuTTY-Configuration_2013-03-05_22-52-01-450x432.png 450w, /wp-content/uploads/2013/03/PuTTY-Configuration_2013-03-05_22-52-01.png 456w" sizes="(max-width: 450px) 100vw, 450px" />][1]

For the log file name, Putty supports the following substitutes.

&H - Hostname  
&Y - Year (yyyy)  
&M - Month (mm)  
&D - Day (dd)  
&T - Time (hhmmss)

D:\Users\username\Dropbox\backup\putty-log\&H-&Y&M&D-&T.log

This will log all your sessions into a [dropbox][2] backup folder with the desired naming format. .i.e "hostname-20130305-132319.log"

Go to "Session" , select the "Default Settings" saved session and hit "save" to make this default for all your new sessions.

NOTE: All your previous saved sessions will need to manually updated.

 [1]: /wp-content/uploads/2013/03/PuTTY-Configuration_2013-03-05_22-52-01.png
 [2]: http://db.tt/MPUL3zQ