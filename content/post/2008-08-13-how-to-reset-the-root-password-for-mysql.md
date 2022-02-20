---
title: How to reset the root password for MySQL
author: Danesh
date: 2008-08-13T10:09:40+00:00
url: /posts/how-to-reset-the-root-password-for-mysql/
robotsmeta:
  - index,follow
pvc_views:
  - 4808
dsq_thread_id:
  - 895416504

---
It happens, you set a super complicated password for your MySQL root account and 2 months down the road forget what it was.

Here&#8217;s how you&#8217;d fix that.

1. Stop your current MySQL database if it is running

`root@abubu# service mysqld stop`

2. Start MySQL in safe mode and bypass reading the privilege table.

`root@abubu# mysqld_safe --skip-grant-tables`

3. Reset your root password MySQL console. If it goes well you will not need to key in a password.

`root@abubu# mysql -u root mysql`

`mysql> update user set Password=PASSWORD('new-password');<br />
mysql> flush privileges;<br />
mysql exit;`

4. Kill the MySQL process and restart MySQL normally.