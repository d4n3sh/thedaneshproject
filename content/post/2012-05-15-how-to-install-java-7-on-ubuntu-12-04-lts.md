---
title: How to install Java 7 on Ubuntu 12.04 LTS
author: Danesh
date: 2012-05-14T21:00:50+00:00
url: /posts/how-to-install-java-7-on-ubuntu-12-04-lts/
pvc_views:
  - 25327
dsq_thread_id:
  - 889761252

---
[<img loading="lazy" class="alignnone size-medium wp-image-2471" title="Java-7-install-check" src="/wp-content/uploads/2012/05/Java-7-install-check-450x249.png" alt="" width="450" height="249" srcset="/wp-content/uploads/2012/05/Java-7-install-check-450x249.png 450w, /wp-content/uploads/2012/05/Java-7-install-check.png 503w" sizes="(max-width: 450px) 100vw, 450px" />][1]

Oracle JDK is no longer included by default in Ubuntu&#8217;s repositories due to licensing. OpenJDK is default now but many apps still don&#8217;t play nice with it. This is why I installed Oracle JDK.

I&#8217;ll walk you through the process of installing Oracle JDK 7 on Ubuntu 12.04 LTS Precise Pangolin, the easy way. For this we will use the &#8220;install oracle-java7-installer&#8221; package from &#8220;WEBUPD8&#8221;.

The &#8220;install oracle-java7-installer&#8221; package from &#8220;WEBUPD8&#8221; will download the official binaries from Oracle and install the JAVA 7 JDK, JRE and browser plugins on your machine.

1. Add the &#8220;WEBUPD8&#8221; PPA.

    danesh@python:~$sudo add-apt-repository ppa:webupd8team/java 

2. Update your repositories.

    danesh@python:~$sudo apt-get update 

3. Install JAVA 7 JDK.

    danesh@python:~$sudo apt-get install oracle-java7-installer

To uninstall,

    sudo apt-get remove oracle-java7-installer

Did it work for you? [Test here][2]

 [1]: /wp-content/uploads/2012/05/Java-7-install-check.png
 [2]: http://www.java.com/en/download/testjava.jsp "Test your Java install"