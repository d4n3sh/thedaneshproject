---
title: How to install Google Chrome on Fedora 16
author: Danesh
date: 2011-11-09T12:09:39+00:00
pvc_views:
  - 11713
dsq_thread_id:
  - 889723770

---
Fedora 16 just came out and here's how to get Google Chrome on it.

Start by creating a repository file for Google called google.repo and place it in /etc/yum.repos.d/ .

`sudo vim /etc/yum.repos.d/google.repo<br />
` 

Add the lines below into the repository file. google.repo

`[google-chrome]<br />
name=google-chrome - 64-bit<br />
baseurl=http://dl.google.com/linux/chrome/rpm/stable/x86_64<br />
enabled=1<br />
gpgcheck=1<br />
gpgkey=https://dl-ssl.google.com/linux/linux_signing_key.pub`

Update yum,  
`sudo yum update`

Search for Google Chrome,  
`sudo yum search google-chrome`

Install Google Chrome Stable  
`sudo yum install google-chrome-stable`

If you prefer the beta like me then run,  
`sudo yum install google-chrome-beta`