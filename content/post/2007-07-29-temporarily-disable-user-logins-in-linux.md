---
title: Temporarily disable user logins in Linux
author: Danesh
date: 2007-07-29T12:27:19+00:00
url: /posts/temporarily-disable-user-logins-in-linux/
pvc_views:
  - 13905
dsq_thread_id:
  - 889736898

---
As a Linux administrator it is sometimes necessary to stop users from login in to your box. This scenario is typically seen during system maintenance cycles, critical updates or scheduled/unscheduled software installs.

The easiest way to accomplish this is to simply create a nologin file in /etc/ .

To stop users from login in run the following command.

    # touch /etc/nologin

To reverse the effect and allow users to log in run the following command.

    # rm /etc/nologin

The above commands work fine on my CenOS5 and openSUSE 10.2 machines.