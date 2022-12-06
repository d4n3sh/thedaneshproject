---
author: "Danesh Manoharan"
title: "2022 12 06 Disabling Google Analytics on Tdp"
date: 2022-12-06T11:12:01+08:00
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
- google
- howto
type: post
lastmod: 2022-12-06T11:12:01+08:00
draft: false
---

I don't monetize this blog, so there is no need for Google Analytics tracking.

I am running the [papermod](https://github.com/adityatelange/hugo-PaperMod) theme.

Here's how I disabled tracking on my blog.

1. Edit the `config.yml` file.
2. Comment out the Google analytics line.
`#googleAnalytics: G-6L9QBHWEKX`
3. Commit and wait for the pipeline to push out the changes.
4. Verify that no Google tracking is getting picked up now.
