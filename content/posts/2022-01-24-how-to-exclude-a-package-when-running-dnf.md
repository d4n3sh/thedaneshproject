---
title: How to exclude a package when running DNF
author: Danesh
date: 2022-01-24T15:44:22+00:00
publishdate: 2022-01-24
lastmod: 2022-01-24
draft: false
tags: [linux]
categories: []
---
I like keeping my workstation updated but prefer to leave the reboots for the weekends. So, I tend to ignore kernel packages when I run my updates.

This is the way,

`sudo dnf update --exclude="kernel*"`
