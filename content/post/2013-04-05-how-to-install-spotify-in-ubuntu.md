---
title: How To Install Spotify In Ubuntu
author: Danesh
date: 2013-04-05T15:31:03+00:00
url: /posts/how-to-install-spotify-in-ubuntu/
dsq_thread_id:
  - 1188807914

---
Follow this guide and you&#8217;ll get to enjoy Spotify&#8217;s Linux client. Note that it&#8217;s a preview release and is unsupported.

Create a new source file for the Spotify repository.

`# sudo vi /etc/apt/sources.list.d/spotify.list<br />
`  
Add the following line into the source file.

Add Spotify&#8217;s public key so that you can verify Spotify&#8217;s packages.  
`sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 94558F59`

`deb http://repository.spotify.com stable non-free<br />
`  
Update your sources

`#sudo apt-get update<br />
`  
Install Spotify

`#sudo apt-get install spotify-client<br />
`  
Source: [Spotify][1]

 [1]: https://www.spotify.com/us/download/previews/ "Spotify Linux Preview"