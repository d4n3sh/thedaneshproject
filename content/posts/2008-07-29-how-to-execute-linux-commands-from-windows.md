---
title: How To Execute Linux commands from Windows
author: Danesh Manoharan
date: 2008-07-28T16:35:11+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 13067
dsq_thread_id:
  - 890122420

---
Most of the time, users are having a Windows Machine on their desk or laptop. Normally, we want to perform a full scale data retrieval from our Linux servers in the DC, where we don't have a trusted Linux server to manage it....the answer to it is use "PLINK" utility.

<a title="Plink Download" href="http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html" target="_blank">Plink </a>comes together with the Putty...

A simple example of usage is:

_**C:\> plink USERNAME@SERVERNAME 'YOUR-LINUX-COMMAND'**_

If you have a dozen of servers...then you probably want to write a batch script in Windows to loop through a list of servers and mention the list of commands juz like what i did.....

Here a typical windows batch script:

_**@echo off**_

_**for / f "tokens=*" %%A in (your-server-list.txt) ( C:\path\to\plink.exe user@server -w YOUR-PASSWORD -m linuxcommandscript > YOUR\_OUTPUT\_FILE.txt)**_

There you go, i did this for my sar report data collection for root cause analysis and infrastructure load analysis....keying in a password wif every darn login is impractical and yet you dont want to generate a security key for the servers.