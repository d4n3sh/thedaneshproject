---
title: Vista not working with DHCP
author: Danesh
date: 2007-02-04T01:44:31+00:00
pvc_views:
  - 87603
dsq_thread_id:
  - 889736262

---
[<img src="/techblog/wp-content/uploads/2007/02/my-vista-20070203.thumbnail.jpg" alt="my-vista-20070203.jpg" title="my-vista-20070203.jpg" align="left" />][1]Just had my Dell Latitude D610 upgraded to Vista Enterprise. Smooth graphics, good speed, good security (small box pops up each time you do something like install apps or change settings, just like Linux) and the side bar's pretty sweet too.

Even with all the above I still prefer my openSUSE 10.2 with XGL and [Beryl][2], It makes Vista look like a kitten. What did they put into all the source code?

Personally I feel that Vista ain't as user friendly as I expected it to be or as they claimed it to be. It's hard to find what you need when you need it.

Hit my first bug when I got back. My Intel pro 2200 BG wireless connection was not getting DHCP lease from my [IPCOP][3] server. The weird thing was that my LAN card was fine and my wireless connection worked fine if I used a static IP.

Spent a whole night trying to feagure out the problem.Good news is I manged to fix it with some help from [MS knowledgebase][4] and a few registry tweaks. It seems to be a problem with the BROADCAST flag in DHCP discovery packets. In XP it's off and in Vista it's on. Non Microsoft DHCP servers don't like this.

See the fix on the next page;<!--more-->

[![my-vista-fix-20070203.jpg][5]][6]

1. Start -> run -> regedit.exe  
2. HKEY\_LOCAL\_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces\{GUID}  
3. {GUID} sub-key refers to the network adapter that is having the issue. In my case my Intel Pro 2200BG card.  
4. Add a new DWORD (32bit) value and rename it to "DhcpConnDisableBcastFlagToggle".  
5. Modify the "DhcpConnDisableBcastFlagToggle" key and change the value to "1".  
6. Modify the "DhcpConnForceBroadcastFlag" key and change the value to "0".  
7. Reboot and test the connection again with DHCP. (The reboot is optional)

[Read the full article at Microsoft][4]

 [1]: /techblog/wp-content/uploads/2007/02/my-vista-20070203.jpg "my-vista-20070203.jpg"
 [2]: http://www.beryl-project.org/
 [3]: http://www.ipcop.org/
 [4]: http://support.microsoft.com/kb/928233/en-us
 [5]: /techblog/wp-content/uploads/2007/02/my-vista-fix-20070203.jpg
 [6]: /techblog/wp-content/uploads/2007/02/my-vista-fix-20070203.jpg "my-vista-fix-20070203.jpg"