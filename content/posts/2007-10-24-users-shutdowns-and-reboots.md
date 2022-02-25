---
title: Users, Shutdowns and Reboots
author: Danesh
date: 2007-10-24T09:29:45+00:00
pvc_views:
  - 6133
dsq_thread_id:
  - 889737866

---
The &#8220;last&#8221; command. Not many people I know use it but there are a quite a few things one could do with it often. Let&#8217;s look at users, shutdowns and reboots.

The &#8220;last or lastb&#8221; command is typically used to show a listing of the last logged in/out users. To view when a particular user last logged in run &#8220;last [username]&#8221;. See output below.

<pre>[root@nosebleed ~]# last danny
danny    pts/1        ftmtj1s.crib     Wed Oct 24 16:51   still logged in
danny    pts/0        python.crib      Wed Oct 24 16:10   still logged in
danny    pts/0        ftmtj1s.crib     Wed Oct 24 14:44 - crash  (01:07)
danny    pts/0        python.crib      Tue Oct 23 16:59 - 17:22  (00:22)
danny    pts/2        python.crib      Tue Oct 23 16:25 - down   (00:32)
danny    pts/1        python.crib      Tue Oct 23 16:09 - down   (00:47)
danny    pts/1        python.crib      Tue Oct 23 16:09 - 16:09  (00:00)
danny    pts/0        ftmtj1s.crib     Tue Oct 23 13:22 - down   (03:34)
danny    pts/0        ftmtj1s.crib     Mon Oct 22 01:18 - 01:43  (00:25)
danny    pts/0        ftmtj1s.crib     Sun Oct 21 01:34 - 21:06  (19:31)
danny    pts/0        ftmtj1s.crib     Sat Oct 20 13:58 - 14:01  (00:03)
danny    pts/0        ftmtj1s.crib     Fri Oct 19 16:52 - 00:23  (07:31)
danny    pts/0        python.crib      Fri Oct 19 11:49 - 14:15  (02:25)
danny    pts/0        python.crib      Thu Oct 18 15:27 - 15:37  (00:09)
danny    pts/0        python.crib      Thu Oct 18 15:22 - 15:23  (00:01)
danny    pts/1        192.168.0.65     Thu Oct 18 15:13 - 15:18  (00:05)
danny    pts/1        192.168.0.65     Thu Oct 18 14:38 - 15:13  (00:35)</pre>

Each time time the &#8220;reboot&#8221; command is executed the &#8220;reboot&#8221; user logs in. Running the &#8220;last reboot&#8221; command would then show the last reboot events. See out put below.

<pre>[root@nosebleed ~]# last reboot
reboot   system boot  2.6.18-8.1.14.el Wed Oct 24 15:51          (01:28)
reboot   system boot  2.6.18-8.1.14.el Tue Oct 23 16:59         (1+00:20)
reboot   system boot  2.6.18-8.1.10.el Thu Oct 18 14:30         (5+02:27)
reboot   system boot  2.6.18-8.1.10.el Wed Oct 17 02:05         (1+11:36)
reboot   system boot  2.6.18-8.1.10.el Tue Oct 16 23:00         (1+14:41)
reboot   system boot  2.6.18-8.1.10.el Tue Oct 16 21:05          (01:52)
reboot   system boot  2.6.18-8.1.10.el Fri Oct 12 22:27         (3+16:41)</pre>

If you only need halt and shutdown information. Running &#8220;last -x | grep down&#8221; will do that. See output below.

<pre>[root@nosebleed ~]# last -x | grep down
shutdown system down  2.6.18-8.1.10.el Tue Oct 23 16:58 - 17:22 (1+00:24)
danny    pts/2        python.crib      Tue Oct 23 16:25 - down   (00:32)
danny    pts/1        python.crib      Tue Oct 23 16:09 - down   (00:47)
danny    pts/0        ftmtj1s.crib     Tue Oct 23 13:22 - down   (03:34)
shutdown system down  2.6.18-8.1.10.el Thu Oct 18 13:42 - 16:57 (5+03:15)
danny    pts/3        ftmtj1s.crib     Thu Oct 18 13:28 - down   (00:12)
danny    pts/2        ftmtj1s.crib     Thu Oct 18 13:11 - down   (00:30)
danny    pts/1        192.168.0.65     Thu Oct 18 00:51 - down   (12:49)
danny    pts/0        192.168.0.65     Wed Oct 17 22:08 - down   (15:32)
shutdown system down  2.6.18-8.1.10.el Tue Oct 16 22:58 - 13:41 (1+14:42)
root     tty1                          Tue Oct 16 21:06 - down   (01:51)
shutdown system down  2.6.18-8.1.10.el Tue Oct 16 15:09 - 22:58  (07:48)
danny    pts/0        192.168.0.65     Tue Oct 16 15:04 - down   (00:04)
shutdown system down  2.6.18-8.1.10.el Fri Oct 12 22:25 - 15:08 (3+16:43)</pre>

Hope this helped, drop me a comment if you need info.