---
title: SSH Tunneling with Putty | Linux
author: Danesh
date: 2007-03-13T06:58:56+00:00
pvc_views:
  - 48446
dsq_thread_id:
  - 889737832

---
SSH tunneling or also known as port forwarding is a way of forwarding normally insecure TCP traffic through SSH. Common ports for example POP3,SMTP,HTTP and FTP can be easily tunneled using SSH.

SSH tunneling is also sometimes used to bypass firewalls where certain ports are blocked.

The figure below represents the network setup at my workplace where the only port available to use is SSH port 22. By implementing portwarding over ssh I am able to port forward Oracle traffic over port 22 to my Oracle DB database running on my private VM with host only networking enabled.

![SSH Tunneling][1] 

In this post I will show you how to apply SSH tunneling using the windows SSH client Putty. I'll cover the Linux implementation in my future post.

<!--more-->

You will need Putty to get started. Putty is a popular free win32 based SSH/Telnet client. Obtain the latest version 0.59 at the homepage.

[Putty Home][2] | [Putty Download][3]

Run Putty, key in the address for your Linux box. In this example &#8220;10.99.34.6&#8221; &#8220;Pandora&#8221; is the Linux box hosting VM and on the VM &#8220;192.168.66.100&#8221; the is an Oracle database running on RHEL 3. The VM is setup with host only networking so it has no access beyond the host machine &#8220;Pandora&#8221;.

[![putty1.png][4]][5]

Look for the SSH tree entry in the menu to the left. Expand it and go to &#8220;Tunnels&#8221;.

[![putty2.png][6]][7]

Fill the the required information and click add.

**Source Port:** 1521  
**Destination:** 192.168.66.100:1521

&#8220;Source port&#8221; is the port Putty will listen on for incoming connections.  
&#8220;Destination&#8221; is the destination port we are trying to access. In this example the Oracle listener is listening on port 1521 for incoming traffic so we use that.  
&#8220;1521&#8221; is the standard Oracle listener port.

[![putty3.png][8]][9]

Remember to save the session in the session page.

Open Putty and login to the Linux box &#8220;Pandora&#8221; and port forwarding should be up.

That's it, have fun.

 [1]: /wp-content/uploads/2007/03/ssh-tunnelling.jpg "SSH Tunneling"
 [2]: http://www.chiark.greenend.org.uk/~sgtatham/putty/
 [3]: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
 [4]: /wp-content/uploads/2007/03/putty1.png
 [5]: /wp-content/uploads/2007/03/putty1.png "putty1.png"
 [6]: /wp-content/uploads/2007/03/putty2.png
 [7]: /wp-content/uploads/2007/03/putty2.png "putty2.png"
 [8]: /wp-content/uploads/2007/03/putty3.png
 [9]: /wp-content/uploads/2007/03/putty3.png "putty3.png"