---
title: How to install Java 7 on Ubuntu 12.04 LTS
author: Danesh Manoharan
date: 2012-05-14T21:00:50+00:00
pvc_views:
  - 25327
dsq_thread_id:
  - 889761252

---
![](/wp-content/uploads/2012/05/Java-7-install-check-450x249.png)

Oracle JDK is no longer included by default in Ubuntu's repositories due to licensing. OpenJDK is default now but many apps still don't play nice with it. This is why I installed Oracle JDK.

I'll walk you through the process of installing Oracle JDK 7 on Ubuntu 12.04 LTS Precise Pangolin, the easy way. For this we will use the "install oracle-java7-installer" package from "WEBUPD8".

The "install oracle-java7-installer" package from "WEBUPD8" will download the official binaries from Oracle and install the JAVA 7 JDK, JRE and browser plugins on your machine.

1. Add the "WEBUPD8" PPA.

    danesh@python:~$sudo add-apt-repository ppa:webupd8team/java 

2. Update your repositories.

    danesh@python:~$sudo apt-get update 

3. Install JAVA 7 JDK.

    danesh@python:~$sudo apt-get install oracle-java7-installer

To uninstall,

    sudo apt-get remove oracle-java7-installer

Did it work for you? [Test here][2]

 [1]: /wp-content/uploads/2012/05/Java-7-install-check.png)
 [2]: http://www.java.com/en/download/testjava.jsp "Test your Java install"
