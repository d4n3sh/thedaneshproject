---
title: Screen | Linux Command
author: Danesh
date: 2007-02-26T10:07:57+00:00
pvc_views:
  - 28515
dsq_thread_id:
  - 889729618

---
When you run commands and programs in a command prompt on Linux, the programs or commands only run while the command prompt session is open but as soon as the command prompt session is terminated for whatever reason, the commands or programs running within the command prompt session will also get terminated.

I use wget to download files from the internet using my [putty][1] console all the time. Imagine downloading a 500mb file and then suddenly [putty][1] crashes causing my session to terminate along with it. There goes my 500mb file download!! I so wished I had known about the &#8220;Screen&#8221; program then.

The screen program is a magnificent utility. Screen basically starts a session within the the session that you logged in with. So, if your putty session suddenly crashed don't worry, the screen session would still be running in the background. Log in again to the server using [putty][1] and you should be able to retrieve the screen session you initiated earlier.

**\# screen**

This starts a screen session.

**\# Ctrl + A followed by D**

This will detach your screen session and return you to the original session you logged in with. Your screen session will now be running in the background.

**\# screen -r**

This command will resume your previous screen session.

**\# Ctrl + A followed by Ctrl + \(back slash)**  
 **\# exit**

You could run either command above to end a screen session.

**\# Ctrl + A followed by &#8220;**

This command will list all the available screen sessions running if there are.

Usefull Links:[  
O'REILLY Linux Command Directory][2]  
Inside Open Source

 [1]: http://www.chiark.greenend.org.uk/~sgtatham/putty/
 [2]: http://www.oreillynet.com/linux/cmd/cmd.csp?path=s/screen