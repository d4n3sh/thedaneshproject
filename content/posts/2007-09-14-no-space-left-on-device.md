---
title: No space left on device
author: Danesh Manoharan
date: 2007-09-14T12:44:18+00:00
pvc_views:
  - 15113
dsq_thread_id:
  - 889737047

---
The DBA I work with was reporting this error on the server she was working on. Every time she tried to add a new cron job the error would come up.

> <p class="MsoNormal">
>   <strong><span style="font-size: 10pt; font-family: 'Courier New'; color: red" lang="PT-BR">[oracle@###### - /db/home/oracle]<o></o><br /> $ crontab -e<o></o><br /> crontab: installing new crontab<o></o><br /> cron/tmp.5821: No space left on device<o></o><br /> crontab: edits left in /tmp/crontab.5821</span></strong>
> </p>

<p class="MsoNormal">
  From the error it's quite obvious that it's a space related issue. It's not fun when you get woken up at 3am but anyway this is how I fixed the problem.<!--more-->
</p>

<p class="MsoNormal">
  First I had to see what the space situation was on the server. Running "df -h" showed sufficient free space available on the server so apparently storage space was not the issue.
</p>

Next I ran "df -i" and the result painted a different picture instead, the server had hit the maximum inodes allowed for the "/var" partition. [What are inodes?  
][1]  
[![][2]][3] [![][4]][5] [![][6]][7]

Ok, so now I know the issue was in "/var". There's most likely a directory within "/var" with a whole bunch of files in it causing the problem.

Running "find /var -size -8k" would return me all files within "/var" smaller then 8k. What I found was a long list of unsent mails in the "/var/spool/mquee" directory. 261517 files to be exact.

How I got "261517" ?

> find /var/spool/mquee -size -8k | wc -l

The next step was to remove all these files. The "rm" command would not work because the amount files I was trying to delete would exceed the maximum argument count allowed for "rm".

[![][8]][9]

A different approach had to be taken. The command would search for files within "/var/spool/mquee" that were smaller then 8k and removed them 1 by 1.

> find /var/spool/mqueue -size -8k -exec rm -f {} \;

The command ran for 30 minutes and fixed the problem and now I have a happy DBA again.

Have you faced familiar situations before? I would love to hear about them and how you fixed them.

 [1]: http://www.google.com/url?sa=t&ct=res&cd=1&url=http%3A%2F%2Fen.wikipedia.org%2Fwiki%2FInode&ei=iX_qRo73DpecgQO3z4zMBg&usg=AFQjCNFS15lNcW09k9Cz2nvOs9Cb4EhxDA&sig2=QPfVs13Tnvl0-iUpk6xBFA
 [2]: http://img462.imageshack.us/img462/4995/inode1cw0.th.png
 [3]: http://img462.imageshack.us/img462/4995/inode1cw0.png
 [4]: http://img462.imageshack.us/img462/8674/inode2lm8.th.png
 [5]: http://img462.imageshack.us/img462/8674/inode2lm8.png
 [6]: http://img462.imageshack.us/img462/3202/inode3xt0.th.png
 [7]: http://img462.imageshack.us/img462/3202/inode3xt0.png
 [8]: http://img142.imageshack.us/img142/9492/node6ci2.th.png
 [9]: http://img142.imageshack.us/img142/9492/node6ci2.png