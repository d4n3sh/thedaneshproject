---
title: Setting the root password on MySQL
author: Danesh
date: 2007-01-23T15:55:54+00:00
pvc_views:
  - 20157
dsq_thread_id:
  - 889736444

---
I just installed [MySQL][1] version 4.1.20 on my [CentOS][2] 4.4 server. The default install of MySQL server uses a blank password for root so I had to have it changed. I also set the MySQL service to start up every time my machine boots up.

This is how I did it;

**Method 1**

1. # yum -y install mysql-server (This will install the mysql binaries)  
2. # chkconfig mysqld on (Adds mysqld to the startup services)  
3. # service mysqld start (Starts the MySQL server)  
4. # mysql -u root@localhost (Brings up the MySQL console)  
5. #mysql> set password for root=password(&#8216;password'); (Sets the root password to &#8220;password&#8221;)  
6. #mysql> reload privileges; (Reloads the grant tables)

**Method 2**

1. # mysql -u root (Brings up the MySQL console)  
2. #mysql> use mysql (Use the mysql database)  
3. #mysql> update user  
-> set password=password(&#8220;password&#8221;) (Sets the root password to &#8220;password&#8221;)  
-> where user=&#8221;root&#8221;;  
4. # reload privileges; (Reloads the grant tables)  
That's it, the next time you want to get the MySQL console up you'll have to run #mysql -u root -p to get the password prompt.

 [Post-Installation Setup and Testing at MySQL][3]

**Update:**

This will work too.

/usr/bin/mysqladmin -u root password &#8216;new-password'  
/usr/bin/mysqladmin -u root -h pandora.crib password &#8216;new-password'

 [1]: http://www.mysql.com/
 [2]: http://centos.org/
 [3]: http://dev.mysql.com/doc/refman/5.0/en/post-installation.html