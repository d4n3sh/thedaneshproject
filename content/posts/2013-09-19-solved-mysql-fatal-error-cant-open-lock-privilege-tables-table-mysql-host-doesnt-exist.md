---
title: 'Solved: mysql  Fatal error: Can’t open and lock privilege tables: Table ‘mysql.host’ doesn’t exist'
author: Danesh Manoharan
date: 2013-09-19T15:16:16+00:00
---
![mysql-logo](/wp-content/uploads/2013/09/mysql-logo.jpg)

Ran into a mysql issue at work today after an unplanned power outage took the server down. The error was _"**Fatal error: Can’t open and lock privilege tables: Table ‘mysql.host’ doesn’t exist"**_ everytime we tried to start mysql. Looked like the system tables were gone.

**The fix;**

We recreated the system tables in the mysql data directory using mysql\_install\_db.

`mysql_install_db –user=mysql –ldata=/mysql-data/location`

Restart mysql and you should be good to go.
