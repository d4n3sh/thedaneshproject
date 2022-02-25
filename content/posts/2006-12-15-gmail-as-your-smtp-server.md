---
title: Gmail as your SMTP server
author: Danesh Manoharan
date: 2006-12-15T10:02:19+00:00
pvc_views:
  - 7758
dsq_thread_id:
  - 889736607

---
<img align="left" alt="Gmail" id="image9" title="Gmail" src="/techblog/wp-content/uploads/2006/12/gmail-logo.jpg" /> Have you installed software that required you to have a SMTP server for it to send out updates by mail? This has always been an issue for me but I've always managed to find a server with some research. Another scenario who be for people who are constantly traveling, they'd have problems when working on different networks by different ISPs.

Google offers a portable SMTP server(freebie) to send mail from any network to any email address provided you have a [Gmail][1] Account.

This is how your get it setup;

1. In your mail applications set the SMTP server for outgoing mail to smtp.google.com .  
2. Make sure username and password options are checked. Input your username [yourgmailname]@gmail.com.  
3. Check off "TLS" under "Use secure connection".

Hope it works for you.

 [1]: http://mail.google.com/mail/ "Gmail"