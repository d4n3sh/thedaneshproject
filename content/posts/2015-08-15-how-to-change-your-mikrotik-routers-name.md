---
title: How to change your MikroTik router’s name
author: Danesh Manoharan
date: 2015-08-15T02:11:37+00:00
dsq_thread_id:
  - 4034066041

---
Via Web or WinBox

System > Identity

![Change MikroTik Hostname via WinBox](/wp-content/uploads/2015/08/mikrotik-change-hostsname-winbox-450x254.png)

If you prefer the Terminal

```
[admin@oldname] > system identity print  
[admin@oldname] > system identity set name=newname  
[admin@oldname] > system identity print
```

![Change MikroTik Hostname](/wp-content/uploads/2015/08/mikrotik-change-hostsname.png)
