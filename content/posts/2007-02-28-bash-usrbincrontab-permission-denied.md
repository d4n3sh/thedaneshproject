---
title: '-bash: /usr/bin/crontab: Permission denied'
author: Danesh
date: 2007-02-27T16:36:32+00:00
pvc_views:
  - 18630
dsq_thread_id:
  - 889736450

---
_&#8221; -bash: /usr/bin/crontab: Permission denied &#8220;._

I was getting this error earlier today while trying to add cron jobs for my login on my [SLES 10][1] box at work. Turns out that all users in [SLES 10][1] by default have no access to cron.

The fix is to add the user to the &#8220;trusted&#8221; group in the group file (/etc/group). Let's assume mu login is &#8220;elf&#8221;.

1. Make sure you are &#8220;root&#8221;.

2. **_#usermod -G trusted elf_**  
This will add the user to the &#8220;trusted&#8221; group.

3. **_#id elf_**  
Display groups the user belongs to. Make sure &#8220;trusted&#8221; is on the list too.  
The output might look like this. _&#8220;uid=502(danny) gid=502(users) groups=502(elf),11(trusted)&#8221;_  
4. **_#su &#8211; elf_**  
Change user

5. **_#crontab -e_**  
Add/Remove/Edit user cron jobs.

6. **_#crontab -l_**  
List user scheduled cron jobs

<span style="font-style: italic">Please do comment if you have an alternative way to accomplish this or if I made a mistake.</span>

 [1]: http://www.novell.com/products/server/