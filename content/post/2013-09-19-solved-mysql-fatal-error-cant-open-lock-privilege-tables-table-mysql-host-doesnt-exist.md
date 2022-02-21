---
title: 'Solved: mysql  Fatal error: Can’t open and lock privilege tables: Table ‘mysql.host’ doesn’t exist'
author: Danesh
date: 2013-09-19T15:16:16+00:00
dsq_thread_id:
  - 1777860299

---
<a href="/posts/solved-mysql-fatal-error-cant-open-lock-privilege-tables-table-mysql-host-doesnt-exist/mysql-logo/" rel="attachment wp-att-3326"><img loading="lazy" class="alignnone size-full wp-image-3326" alt="mysql-logo" src="/wp-content/uploads/2013/09/mysql-logo.jpg" width="313" height="161" /></a>

Ran into a mysql issue at work today after an unplanned power outage took the server down. The error was _&#8220;**Fatal error: Can’t open and lock privilege tables: Table ‘mysql.host’ doesn’t exist&#8221;**_ everytime we tried to start mysql. Looked like the system tables were gone.

**The fix;**

We recreated the system tables in the mysql data directory using mysql\_install\_db.

`mysql_install_db –user=mysql –ldata=/mysql-data/location`

Restart mysql and you should be good to go.