---
title: How to configure SSL on Tomcat 5
author: Danesh
date: 2007-12-20T12:00:44+00:00
url: /posts/how-to-configure-ssl-on-tomcat-5/
pvc_views:
  - 28999
dsq_thread_id:
  - 889737262

---
Had to SSL on a test server running Tomcat 5 yesterday. This is how I did it.

  1. >cd _**$CATALINA_HOME**_
  2. > _**$JAVA_HOME/keytool -genkey -alias tomcat -keyalg RSA -keystore mycert.jks**_
  3. Enter keystore password:_  **changeit**_
  4. What is your first and last name? [Unknown]: _**Danesh Manoharan  
**_ 
  5. What is the name of your organizational unit? [Unknown]: _**IT**_
  6. What is the name of your organization? [Unknown]: _**My Comp**_.
  7. What is the name of your City or Locality? [Unknown]: _**KL**_
  8. What is the name of your State or Province? [Unknown]: _**KL**_
  9. What is the two-letter country code for this unit? [Unknown]: _**MY**_
 10. US Is CN=Danesh Manoharan, OU=IT, O=&#8221;My Comp.&#8221;, L=KL, ST=KL, C=MY correct? [no]: _**yes**_
 11. Enter key password for <tomcat> (RETURN if same as keystore password): Hit Enter.</tomcat>

Tomcat will assume the password is &#8220;changeit&#8221; by default so it&#8217;s advised to leave it that way. Now let&#8217;s tell Tomcat to use the keystore file.

  1. cd $CATALINA_HOME/conf/
  2. vi server.xml
  3. Look for &#8220;<!&#8211; Define a SSL HTTP/1.1 Connector on port 8443 &#8211;>&#8221;. Remove the <!&#8211; &#8211;> comments indicator and add the keystore info.

> <!&#8211; Define a SSL HTTP/1.1 Connector on port 8443 &#8211;>  
> <Connector port=&#8221;_**443**_&#8221; maxHttpHeaderSize=&#8221;8192&#8243;  
> maxThreads=&#8221;150&#8243; minSpareThreads=&#8221;25&#8243; maxSpareThreads=&#8221;75&#8243;  
> enableLookups=&#8221;false&#8221; disableUploadTimeout=&#8221;true&#8221;  
> acceptCount=&#8221;100&#8243; scheme=&#8221;https&#8221; secure=&#8221;true&#8221;  
> keystoreFile=&#8221;_**/opt/Tomcat5/mycert.jks**_&#8221;  
> clientAuth=&#8221;false&#8221; sslProtocol=&#8221;TLS&#8221; />

Time to restart Tomcat and test.

  1. cd $CATALINA_HOME/bin/
  2. ./shutdown.sh to make sure Tomcat is down.
  3. ./startup.sh to start Tomcat.
  4. Fire up your browser and test your new https site. _**https://localhost/**_