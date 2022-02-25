---
title: Installing Pidgin on openSUSE 10.2
author: Danesh Manoharan
date: 2007-07-14T21:04:20+00:00
pvc_views:
  - 6421
dsq_thread_id:
  - 889737110

---
Decided to install Pidgin on my notebook running openSUSE 10.2 today. If you didn't already know Pidgin was previously know as GAIM.

The install was pretty simple but I decided to share it with you anyway. If you are new to openSUSE then this may come in handy.

To start off you will need to get the following repository added to YaST. Start -> Computer -> Administrator Settings(Yast) -> Software -> Installation Source .

Protocol : HTTP  
Server : software.opensuse.org  
Directory : /download/GNOME:/Community/openSUSE_10.2/[][1]

[![snapshot5.png][2]][3][][1]

[![snapshot4.png][4]][5]

<!--more-->Next step is to install the Pidgin package using YaST. Strart -> Computer -> Administrator Settings (Yast) -> Software Management .

Search for "Pidgin" in the search box and then look for "Pidgin" in he result box to the right. Select Pidgin and libpurple and hit the Accept button.

[![snapshot1.png][6]][7]

That's it for the install portion. You now have Pidgin installed. Let's start it up.

Start -> Applications -> Internet -> Chat -> Pidgin .

Launching Pidgin for the first time will bring up the accounts maintenance page. Start adding your accounts.

[![snapshot2.png][8]][9]

[![snapshot6.png][10]][11]

Once you are done with the accounts Pidgin should launch. That's it, you have successfully installed Pidgin.

[![snapshot3.png][12]][1]

I personally feel that Pidgin feels like [Gtalk][13] but I love the [Gtalk][13] interface so I can't complain. Clean, simple yet elegant.

Some cool Pidgin plugins you would want to try.

  * [Guifications for Pidgin][14] 
  * [30+ plugins for Pidgin][15]

Sources:

  * [Pidgin Home][16]
  * [i-nZ BLoG][17]
  * [Kenno's OpenNote][18]
  * [openSUSE][19]

 [1]: /wp-content/uploads/2007/07/snapshot3.png "snapshot3.png"
 [2]: /wp-content/uploads/2007/07/snapshot5.thumbnail.png
 [3]: /wp-content/uploads/2007/07/snapshot5.png "snapshot5.png"
 [4]: /wp-content/uploads/2007/07/snapshot4.thumbnail.png
 [5]: /wp-content/uploads/2007/07/snapshot4.png "snapshot4.png"
 [6]: /wp-content/uploads/2007/07/snapshot1.thumbnail.png
 [7]: /wp-content/uploads/2007/07/snapshot1.png "snapshot1.png"
 [8]: /wp-content/uploads/2007/07/snapshot2.thumbnail.png
 [9]: /wp-content/uploads/2007/07/snapshot2.png "snapshot2.png"
 [10]: /wp-content/uploads/2007/07/snapshot6.thumbnail.png
 [11]: /wp-content/uploads/2007/07/snapshot6.png "snapshot6.png"
 [12]: /wp-content/uploads/2007/07/snapshot3.thumbnail.png
 [13]: http://www.google.com/talk/
 [14]: http://plugins.guifications.org/trac/wiki/Guifications
 [15]: http://plugins.guifications.org/trac/wiki/PluginPack
 [16]: http://pidgin.im/pidgin/home/
 [17]: http://i-nz.net/2007/05/06/pidgin-plugins-opensuse-rpms/
 [18]: http://kenno.wordpress.com/2007/06/10/installing-pidgin-on-opensuse-102/
 [19]: http://www.opensuse.org/