---
title: Duplicate ssh sessions without password prompt
author: Danesh Manoharan
date: 2007-06-15T03:33:08+00:00
pvc_views:
  - 4191
dsq_thread_id:
  - 889737661

---
I work with multiple ssh sessions whenever I connect to a server. Typically I would have about 3 sessions initiated from my host machine to the destination server.

Found away to duplicate my session without retyping my password every time I initiate a connection the the server from my host machine thanks toÂ  [Linux By Examples.][1]

Add the following 2 lines to your /etc/ssh/ssh_config file and feature will be ready for you to use once you restart the sshd service.

_**ControlMaster auto  
ControlPath ~/.ssh/socket-%r@%h:%p**_

[![ssh-dup.jpg][2]][3]

<!--more-->

**ControlMaster**  
Enables the sharing of multiple sessions over aÂ  single  
networkÂ  connection.Â Â  WhenÂ  setÂ  toÂ  "yes"Â  ssh will  
listen for connections on aÂ  controlÂ  socketÂ  specified  
usingÂ  theÂ  ControlPathÂ  argument.Â  Additional sessions  
can connect to this socket using theÂ  sameÂ  ControlPath  
withÂ  ControlMaster set to "no" (the default).Â  These  
sessions will reuse the master instance's networkÂ  con-  
nectionÂ  rather than initiating new ones.Â  Setting this  
to "ask" will cause ssh to listen for control connec-  
tions,Â  butÂ  require confirmation using the SSH_ASKPASS  
program before they are acceptedÂ  (seeÂ  ssh-add(1)Â  for  
details).

**ControlPath**  
SpecifyÂ  theÂ  pathÂ  toÂ  theÂ  controlÂ  socketÂ  usedÂ  for  
connection sharing.Â  See ControlMaster above.

 [1]: http://linux.byexamples.com/archives/286/duplicate-ssh-session/
 [2]: /wp-content/uploads/2007/06/ssh-dup.jpg
 [3]: /wp-content/uploads/2007/06/ssh-dup.jpg "ssh-dup.jpg"