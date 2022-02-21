---
title: How to build a local DNS caching server
author: Danesh
date: 2008-08-28T08:31:01+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 12474
dsq_thread_id:
  - 890830191

---
Being in Malaysia we are gifted with superior Internet speeds. NOT!!

Services like openDNS are awesome but the lag between us and them often results in sluggish performance anyways.

One way to improve performance is to use local DNS servers. I don&#8217;t use Streamyx&#8217;s DNS servers because they SUCK!!. TIME&#8217;s DNS servers are ok but I still prefer openDNS.

To improve performance, I put together a local DNS caching-only server that forwards to openDNS. Now I have openDNS with lighting fast response.

Let&#8217;s walk though the steps to get your own local DNS caching-only server setup. I&#8217;m using openSUSE 11 so the steps might vary depending on your distro.

1. Install BIND

`pandora:~ # zypper in bind`

2. Edit /etc/named.conf

`pandora:~ # vi /etc/named..conf`

Uncomment the **forwarders** section. Update the default values with the values below.

`forwarders { 208.67.222.222; 208.67.220.220; };`  
`<br />
forward only;`

Add the line &#8221; **forward only;** &#8221; This will tell BIND to only forward to the forwarders and not the ROOT servers.

3. Start the service.

To have the service start automatically run &#8221; `chkconfig named on` &#8221;

`pandora:~ # service named start`

4. Let&#8217;s make sure your caching server is running fine.

`pandora:~ # nslookup google.com localhost<br />
Server:Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  localhost<br />
Address:Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  127.0.0.1#53`

`Non-authoritative answer:<br />
Name:Ã‚Â Ã‚Â  google.com<br />
Address: 64.233.167.99<br />
Name:Ã‚Â Ã‚Â  google.com<br />
Address: 72.14.207.99<br />
Name:Ã‚Â Ã‚Â  google.com<br />
Address: 64.233.187.99`  
`<br />
pandora:~ # nslookup yahoo.com localhost<br />
Server:Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  localhost<br />
Address:Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  127.0.0.1#53`

`Non-authoritative answer:<br />
Name:Ã‚Â Ã‚Â  yahoo.com<br />
Address: 68.180.206.184<br />
Name:Ã‚Â Ã‚Â  yahoo.com<br />
Address: 206.190.60.37`

5. Update your /etc/resolv.conf file.

This will tell your system to use the local DNS server which we just setup instead of the external ones.

Add the lines below to the file.

`nameserver 127.0.0.1<br />
nameserver 127.0.0.2`

That&#8217;s it. You now have local DNS caching. Enjoy!!

<!--more-->

My **/etc/named.conf** file. Only the lines I changed.

`#forwarders { 192.0.2.1; 192.0.2.2; };<br />
forwarders { 208.67.222.222; 208.67.220.220; };`

\# Enable the next entry to prefer usage of the name server declared in  
\# the forwarders section.

#forward first;  
forward only;