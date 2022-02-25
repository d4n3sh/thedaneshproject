---
title: How to install ClamAV
author: Danesh Manoharan
date: 2008-08-20T13:28:37+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 7907
dsq_thread_id:
  - 889793952

---
Here a quick walk through on how to install and perform a file system scan with ClamAV. I'll be installing and scanning on a RedHat 7.3 machine.

First download the required files listed below. For other distributions you should refer to the [download page][1] to get the suitable packages. I saved the files to /opt/clamav/

1. clamav (Scanning tools)

2. clamav-db (Virus database)

3. main.cvd (Virus database update file)

4. daily.cvd (Virus database update file)

Let's start installing the packages.

`[root@pinky:~]# rpm -ivh clamav-db-0.93.3-1.rh7.rf.i386.rpm`

[root@pinky:~]# rpm -ivh clamav-0.93.3-1.rh7.rf.i386.rpm

[root@pinky:~]# cp main.cvd /var/clamav/

[root@pinky:~]# cp daily.cvd /var/clamav/

That concludes the install process. Now lets scan.

<!--more-->

First check if your virus database is up to date.

`[root@pinky:~]# freshclam<br />
ClamAV update process started at Wed Aug 20 17:49:38 2008<br />
main.cvd is up to date (version: 47, sigs: 312304, f-level: 31, builder: sven)<br />
daily.cvd is up to date (version: 8058, sigs: 85172, f-level: 33, builder: acab)`

To scan the command would look like this. clamscan \[options\] \[directory\]

The -r option will force the scan to be recursive across directories.

`[root@pinky:~]# clamscan -r /home/`

The -i option will only return infected files.

`[root@pinky:~]# clamscan -r -i /home/`

You can also use -move=[directory] to move infected files or -copy=[directory] to copy infected files to a designated directory.

`[root@pinky:~]# clamscan -r -i --move=/infected-files/`

[root@pinky:~]# clamscan -r -i -copy=/infected-files/

To save the scan summary to a report file user -l /scan/report/scan.log or -log=/scan/report/scan.log

`[root@pinky:~]# clamscan -r -i --log=/scan/report/scan.log`

Sample scan summary,

`[root@pinky:~]#`

———- SCAN SUMMARY ———-  
Known viruses: 396679  
Engine version: 0.93.3  
Scanned directories: 1920  
Scanned files: 25372  
Infected files: 6  
Data scanned: 6643.96 MB  
Time: 3020.422 sec (50 m 20 s)

 [1]: http://www.clamav.net/download/