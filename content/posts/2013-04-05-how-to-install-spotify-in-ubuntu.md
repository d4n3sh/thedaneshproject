---
title: How To Install Spotify In Ubuntu
author: Danesh Manoharan
date: 2013-04-05T15:31:03+00:00
dsq_thread_id:
  - 1188807914

---
Follow this guide and you'll get to enjoy Spotify's Linux client. Note that it's a preview release and is unsupported.

Create a new source file for the Spotify repository.

`# sudo vi /etc/apt/sources.list.d/spotify.list<br />
`  
Add the following line into the source file.

Add Spotify's public key so that you can verify Spotify's packages.  
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