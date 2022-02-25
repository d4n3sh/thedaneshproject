---
title: Send mail through SMTP using Telnet
author: Danesh Manoharan
date: 2008-04-03T07:58:19+00:00
pvc_views:
  - 109714
dsq_thread_id:
  - 889763925

---
Developers in my office constantly complain that the SMTP server is down and no mails are being sent out. We come back saying that their application is buggy. Most often after hours of troubleshooting the problem will turn out to be the application itself.

Here's a simple way to test your SMTP server over port 25 using Telnet to proof them wrong.

Telnet to the server via port 25.

1. Key in "EHLO example.com" and hit enter.

2. Key in "MAIL FROM: sender@domain.com" and hit enter.

3. Key in "RCPT TO: recipient@domain.com" and hit enter.

4. Key in "DATA" and hit enter.

5. Key in your message body and hit enter.

6. Key in " . " and press enter.

If you received the mail then your SMTP is working fine.

Sample output,  
<!--more-->

  
`<br />
[root@abooboo tmp]# telnet 192.168.0.25 25<br />
Trying 192.168.0.25...<br />
Connected to 192.168.0.25 (192.168.0.25).<br />
Escape character is '^]'.<br />
220 smtp11.klk.example.com Microsoft ESMTP MAIL Service, Version: 5.0.2195.6713 ready at  Thu, 3 Apr 2008 15:39:17 +0800<br />
EHLO Vsource.com<br />
250-smtp11.klk.example.com Hello [192.168.0.192]<br />
250-AUTH GSSAPI NTLM LOGIN<br />
250-AUTH=LOGIN<br />
250-TURN<br />
250-ATRN<br />
250-SIZE<br />
250-ETRN<br />
250-PIPELINING<br />
250-DSN<br />
250-ENHANCEDSTATUSCODES<br />
250-8bitmime<br />
250-BINARYMIME<br />
250-CHUNKING<br />
250-VRFY<br />
250 OK<br />
MAIL FROM: danesh@example.com<br />
250 2.1.0 danesh@example.com....Sender OK<br />
RCPT TO: danesh_manoharan@example.com<br />
250 2.1.5 danesh_manoharan@example.com<br />
DATA<br />
354 Start mail input; end with <crlf>.<crlf><br />
this is a test over SMTP<br />
.<br />
250 2.6.0 <klmdns1fraqbc8wsa1x00000002@smtp11.klk.example.com> Queued mail for delivery<br />
quit<br />
221 2.0.0 smtp11.klk.example.com Service closing transmission channel<br />
Connection closed by foreign host.<br />
[root@abooboo tmp]#</klmdns1fraqbc8wsa1x00000002@smtp11.klk.example.com></crlf></crlf>`

[ [RFC 821][1] ] Thanks Cinod79

 [1]: http://www.ietf.org/rfc/rfc0821.txt