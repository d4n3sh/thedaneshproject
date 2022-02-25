---
title: Deluge 1.0.2 released
author: Danesh Manoharan
date: 2008-10-11T16:19:37+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 3925
dsq_thread_id:
  - 893262989

---
[<img loading="lazy" src="http://farm4.static.flickr.com/3074/2931191393_d9eb5c92c3.jpg" alt="deluge1.0.2" width="500" height="302" />][1]

Deluge 1.0.2 is out. This is an important bug fix release for Deluge 1.0.0. Many bug fixes and stability improvements have gone into it.

Changelog; [Read more][2]

> Deluge 1.0.2 (10 October 2008)  
> Core:  
> * Fix issue where torrents will not be properly added to the session
> 
> Deluge 1.0.1 (10 October 2008)  
> Core:  
> * Change the default max global upload slots to 4 instead of -1 since libtorrent  
> will automatically open more slots to meet the upload speed limit.  
> * Fix display of tracker error messages  
> * Fix add\_torrent\_url() to download the torrent file in a thread to prevent  
> the main thread from blocking and causing the daemon to freeze.  
> * Removed the 'Maximum Connections Per Second' setting and replaced it with a  
> default setting of 20. This should alleviate speed issues some are experiencing.  
> * Changed max half-open connections default limit to 8 on XP/2000 and 4 on Vista  
> * Prevent being able to set file priorities for compactly allocated torrents as  
> it is not intended to work.  
> * Fix freezing on start-up issues on systems that do not have a properly  
> configured localhost entry.  
> * Change max connections default setting to 200  
> * Fix issue with invalid bencoding from some trackers  
> * Plenty of libtorrent updates that should improve core stability
> 
> GtkUI:  
> * Improve performance of files tab by only updating when values change
> 
> Misc:  
> * Fix #187 set a 5 second timer to save the config file after a config value  
> has been changed.  
> * Fix #503 change the boost lib detection logic to first look for -mt and  
> if not available, fall back to regular boost lib (non-multithreaded)
> 
> WebUI:  
> * Add enable "Auto Add" checkbox

[Download Deluge][3]

 [1]: http://www.flickr.com/photos/dannyportal/2931191393/ "deluge1.0.2 by Danesh Manoharan, on Flickr"
 [2]: http://forum.deluge-torrent.org/viewtopic.php?f=8&t=10585
 [3]: http://deluge-torrent.org/downloads.php