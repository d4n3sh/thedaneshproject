---
title: How to change the default web port on unRAID
author: Danesh Manoharan
date: 2016-05-18T07:23:42+00:00
dsq_thread_id:
  - 4857166579

---
{{< figure src="/wp-content/uploads/2016/05/Screenshot-from-2016-05-18-14-55-13.png" alt="unRAID default port change" >}}

You can easily change the default web port for unRAID from port 80 to something you like by changing the "go" file in "/boot/config/". In the example above I changed my unRAID to listen on "8008" instead of the default "80".

You will have to restart your unRAID server to apply the change.
