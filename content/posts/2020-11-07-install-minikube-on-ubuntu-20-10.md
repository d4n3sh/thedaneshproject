---
title: Install minikube on Ubuntu 20.10
author: Danesh Manoharan
date: 2020-11-07T00:33:25+00:00

---
I'm installing minikube on my shiny new Pop!OS 20.10 install which is based on Ubuntu 20.10.

```>_lsb_release -a
No LSB modules are available.
Distributor ID: Pop
Description:    Pop!_OS 20.10
Release:    20.10
Codename:   groovy```

I prefer to have my standalone application binaries placed in ~/.bin/ which is already included in my PATH.

```&gt;_ cd ~/.bin
&gt;_ curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
% Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
Dload  Upload   Total   Spent    Left  Speed
100 53.3M  100 53.3M    0     0  63.9M      0 --:--:-- --:--:-- --:--:-- 63.8M
&gt;_ install -m 775 minikube-linux-amd64 ./minikube
&gt;_ ll
total 343M
drwxrwxr-x 11 danesh danesh 4.0K Oct 11 11:27 fzf
drwxrwxr-x  9 danesh danesh 4.0K Oct 30 14:29 google-cloud-sdk
-rwxrwxr-x  1 danesh danesh  54M Nov  6 18:10 minikube
-rw-rw-r--  1 danesh danesh  54M Nov  6 18:10 minikube-linux-amd64
-rwxr-xr-x  1 danesh danesh 119M Sep 30 12:55 packer
-rwxr-xr-x  1 danesh danesh  82M Sep 30 13:10 terraform
-rwxr-xr-x  1 danesh danesh  37M Aug 24 18:02 vagrant
&gt;_ rm minikube-linux-amd64
```

Verify if it's working

```&gt;_ cd ~
&gt;_ which minikube
/home/danesh/.bin/minikube
&gt;_ source &lt;(minikube completion zsh)
&gt;_ minikube version
minikube version: v1.14.2
commit: 2c82918e2347188e21c4e44c8056fc80408bce10
```