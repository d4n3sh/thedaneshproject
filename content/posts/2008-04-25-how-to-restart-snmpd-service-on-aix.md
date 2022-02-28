---
title: How to restart snmpd service on AIX
author: Danesh Manoharan
date: 2008-04-25T07:35:21+00:00
pvc_views:
  - 30543
dsq_thread_id:
  - 889750987
dsq_needs_sync:
  - 1

---
![](/wp-content/uploads/2008/04/aix_logo1.gif)

This is how you would restart the snmpd service on AIX. 

oslevel is used to return the current OS level. stopsrc -s [service] to stop and startsrc -s [service] to start a service.

`[root@kakuna]:/# oslevel<br />
4.3.3.0<br />
[root@kakuna]:/# stopsrc -s snmpd<br />
0513-044 The snmpd Subsystem was requested to stop.<br />
[root@kakuna]:/# stopsrc -s snmpd<br />
0513-004 The Subsystem or Group, snmpd, is currently inoperative.<br />
[root@kakuna]:/# startsrc -s snmpd<br />
0513-059 The snmpd Subsystem has been started. Subsystem PID is 8004.<br />
[root@kakuna]:/#`