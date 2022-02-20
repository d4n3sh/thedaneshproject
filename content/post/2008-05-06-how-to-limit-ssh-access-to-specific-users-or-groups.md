---
title: How to limit ssh access to specific users or groups
author: Danesh
date: 2008-05-06T02:00:23+00:00
url: /posts/how-to-limit-ssh-access-to-specific-users-or-groups/
pvc_views:
  - 17846
dsq_thread_id:
  - 889978590

---
Its sometimes necessary to limit who has access to a server via SSH. Most Linux security hardening checklist today require this to be enforced.

Fortunately this can be easily done with openSSH. Just edit the /etc/ssh/sshd_config file and add the desired directives shown below. You don&#8217;t need them all, just use what suits you needs.

openSSH provides 4 directives, AllowUsers, AllowGroups, DenyUsers and DenyGroups

`AllowUsers buddy john doe`  
Only users _buddy_, _john_ and _doe_ will be able to log in via ssh.

`AllowGroups sysadmin bkpadmin`  
Only users within groups _sysadmin_ and _bkpadmin_ will be able to log in via ssh.

`DenyUsers rambo tina`  
This is the opposite of AllowUsers. All users except for _rambo_ and _tina_ will be able to log in via ssh.

`DenyGroups hr payroll`  
This is the opposite of AllowGroups. All groups except for _hr_ and _payroll_ will be able to log in via ssh.