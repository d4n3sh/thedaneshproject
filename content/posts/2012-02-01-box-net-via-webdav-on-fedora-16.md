---
title: Box.net via WebDAV on Fedora 16
author: Danesh
date: 2012-02-01T15:24:52+00:00
pvc_views:
  - 5818
dsq_thread_id:
  - 890154167

---
<img loading="lazy" class="alignnone size-medium wp-image-2356" title="boxnet" src="/wp-content/uploads/2012/02/boxnet-450x271.png" alt="" width="450" height="271" srcset="/wp-content/uploads/2012/02/boxnet-450x271.png 450w, /wp-content/uploads/2012/02/boxnet.png 640w" sizes="(max-width: 450px) 100vw, 450px" />  
I was lucky enough to get a <a title="Current 50GB promotions" href="https://support.box.net/entries/20768867-box-50-gb-promotion-faqs" target="_blank">free 50GB box.net</a> account. 50GB is alot!. However, the catch, individual files can't exceed 100mb each. lol

I mainly use my box.net to hold eBooks for later access on my Laptop and Android devices.

There is no free client for Linux so I use WebDAV instead. It's slower but it works.

Start by installing davfs2.  
`# sudo yum install davfs2<br />
` Create your Box.net directory  
`# mkdir ~/Box.net<br />
` Create the davfs2 config directory. It's in your home dir so it's not system wide.  
`# mkdir ~/.davfs2<br />
` Disable locking. Causes issues sometimes.  
`# cd ~/.davfs2<br />
# echo "use_locks 0" > davfs2.conf`  
Create a secret file to hold your box.net login details. Make sure to "chmod 600 the file"  
`# echo "https://www.box.net/dav [you box.net login] [your box.net password]" > secrets<br />
# chmod 600 secrets`  
Backup and update your /etc/fstab file to include your box.net directory.  
`# cp /etc/fstab /etc/fstab.ori<br />
# echo "https://www.box.net/dav /home/danesh/Box.net davfs rw,user,noauto 0 0" >> /etc/fstab`  
Mount and you should be able to list ~/Box.net  
`# mount ~/Box.net<br />
# ls -l ~/Box.net`

This is the hard way to do this. I will post a simpler method using Nautilus in a future post.