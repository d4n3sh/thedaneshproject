---
title: Installing Novell Moonlight on openSUSE 11.1
author: Danesh
date: 2009-03-29T12:48:41+00:00
url: /posts/installing-novell-moonlight-on-opensuse-111/
robotsmeta:
  - index,follow
pvc_views:
  - 5341
dsq_thread_id:
  - 891518892

---
First, make sure you have the [PackMan][1] repo added.

Bring up a console and su to root or use sudo.

Run the commands below;

`zypper -v search moonlight`

`zypper -v install moonlight-plugin`

Sample output;

`pandora:~ # zypper -v search moonlight<br />
S | Name             | Summary                             | Type<br />
--+------------------+-------------------------------------+-----------<br />
| moonlight        | Novell Moonlight                    | srcpackage<br />
| moonlight-plugin | Browser plugin for Novell Moonlight | package<br />
| moonlight-tools  | Various tools for Novell Moonlight  | package` 

pandora:~ # zypper -v install moonlight-plugin

The following NEW packages are going to be installed:  
libmoon0-1.0+final-0.pm.1.i586 (Packman Repository, http://packman.links2linux.de)  
moonlight-plugin-1.0+final-0.pm.1.i586 (Packman Repository, http://packman.links2linux.de)

Overall download size: 1.6 M. After the operation, additional 5.8 M will be used.  
Continue? [YES/no]: yes  
committing  
Retrieving package libmoon0-1.0+final-0.pm.1.i586 (1/2), 1.2 M (4.3 M unpacked)  
Retrieving: libmoon0-1.0+final-0.pm.1.i586.rpm [done (62.4 K/s)]  
Installing: libmoon0-1.0+final-0.pm.1 [done]  
Retrieving package moonlight-plugin-1.0+final-0.pm.1.i586 (2/2), 386.0 K (1.4 M unpacked)  
Retrieving: moonlight-plugin-1.0+final-0.pm.1.i586.rpm [done (52.9 K/s)]  
Installing: moonlight-plugin-1.0+final-0.pm.1 [done]  
committingCommitResult 2 (errors 0, remaining 0, srcremaining 0)  
pandora:~ #

 [1]: http://packman.links2linux.org/