---
author: "Danesh Manoharan"
title: "Change Admin Password on Arista EOS"
date: 2022-03-05T13:01:14-06:00
description: "Change the admin account password on Arista's EOS " # Post description, shows up below title
cover:
    image: "Arista_Logo.png" # image path/url
    alt: "Arista Logo" # alt text
    caption: "Arista Logo" # display caption under cover
    relative: true # when using page bundles set this to true
    hidden: false # only hide on current single page
images:
- 
tags:
- arista
- howto
type: post
lastmod: 2022-03-05T13:01:14-06:00
draft: false
---

```text
localhost> en
localhost# conf
localhost(config)# username admin secret supersecretpassword
```
