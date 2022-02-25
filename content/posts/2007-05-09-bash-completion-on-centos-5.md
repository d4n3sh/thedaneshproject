---
title: Bash Completion on CentOS 5
author: Danesh
date: 2007-05-09T07:19:08+00:00
pvc_views:
  - 16059
dsq_thread_id:
  - 889961760

---
I use the command line everyday at for work and home. Command switches a part of life but the problem is remembering switches. The man files have always helped and always will continue doing so.

[Bash-completion][1] came along to help in this area. It displays a list of a available switched for a specific command by simply hitting the _**TAB key**_ twice. See screenshots below for clearer picture.

1. Download the rpm . Currently no packages available from the CentOS repos.  
_**#"wget http://www.caliban.org/files/redhat/RPMS/noarch/bash-completion-20060301-1.noarch.rpm"**_

2. Install the rpm  
_**#"rpm -ivh bash-completion-20060301-1.noarch.rpm"**_

3. Start a new shell or execute the command below  
_**#". /etc/bash_completion"**_

4. Test out your new shell enhancement  
_**#"ls &#8212; \[TAB\]\[TAB\]"**_

[![bash-completion1.jpg][2]][3]

[![bash-completion2.jpg][4]][5]

Other Sources:

 [All About Linux][6]

[Debian Administration][7]

 [1]: http://freshmeat.net/projects/bashcompletion/
 [2]: /wp-content/uploads/2007/05/bash-completion1.thumbnail.jpg
 [3]: /wp-content/uploads/2007/05/bash-completion1.jpg "bash-completion1.jpg"
 [4]: /wp-content/uploads/2007/05/bash-completion2.thumbnail.jpg
 [5]: /wp-content/uploads/2007/05/bash-completion2.jpg "bash-completion2.jpg"
 [6]: http://linuxhelp.blogspot.com/2005/09/bash-completion-makes-life-easier-for.html
 [7]: http://www.debian-administration.org/articles/316