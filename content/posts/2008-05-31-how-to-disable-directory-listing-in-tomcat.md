---
title: How to disable directory listing in Tomcat
author: Danesh Manoharan
date: 2008-05-30T19:27:47+00:00
---
![tomcat](/wp-content/uploads/2008/05/tomcat1.gif "tomcat")

This is how you turn off directory list for yr Tomcat server.

1. Edit the default servlet in the {$CATALINA_HOME}/conf/web.xml file.

2. Look for the <init-param> section within the <servlet section>

`<servlet><br />
<servlet-name>default</servlet-name><br />
<servlet-class><br />
org.apache.catalina.servlets.DefaultServlet<br />
</servlet-class><br />
<init-param><br />
<param-name>debug</param-name><br />
<param-value>0</param-value><br />
</init-param><br />
<init-param><br />
<param-name>listings</param-name><br />
<param-value>true</param-value><br />
</init-param><br />
<load-on-startup>1</load-on-startup><br />
</servlet>`

3. Change the <param-value> to false for the <param-name>listing</param-name> section.

`<init-param><br />
<param-name>listings</param-name><br />
<param-value>false</param-value><br />
</init-param>`

 [1]: /wp-content/uploads/2008/05/tomcat1.gif