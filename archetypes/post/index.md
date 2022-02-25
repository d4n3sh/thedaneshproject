---
author: "{{ .Site.Params.author }}"
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
description: "" # Post description, shows up below title
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: true # when using page bundles set this to true
    hidden: true # only hide on current single page
images:
- 
tags:
- 
type: post
draft: true
---

