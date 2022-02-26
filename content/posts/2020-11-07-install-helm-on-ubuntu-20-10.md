---
title: Install Helm on Ubuntu 20.10
author: Danesh Manoharan
date: 2020-11-08T02:00:00+00:00

---
Go to the release page to get the download link for the latest version of helm. <https://github.com/helm/helm/releases>

I prefer the binaries to be in my ~/.bin/ directory as it is already in my PATH

```
>_ cd ~/.bin

>_ wget https://get.helm.sh/helm-v3.4.0-linux-amd64.tar.gz
 --2020-11-06 19:41:28--  https://get.helm.sh/helm-v3.4.0-linux-amd64.tar.gz
 Resolving get.helm.sh (get.helm.sh)… 152.195.19.97, 2606:2800:11f:1cb7:261b:1f9c:2074:3c
 Connecting to get.helm.sh (get.helm.sh)|152.195.19.97|:443… connected.
 HTTP request sent, awaiting response… 200 OK
 Length: 13315267 (13M) [application/x-tar]
 Saving to: ‘helm-v3.4.0-linux-amd64.tar.gz’
 helm-v3.4.0-linux-amd64.tar.gz  100%[======================================================>]  12.70M  77.2MB/s    in 0.2s    
 2020-11-06 19:41:29 (77.2 MB/s) - ‘helm-v3.4.0-linux-amd64.tar.gz’ saved [13315267/13315267]
 
>_ tar -zxvf helm-v3.4.0-linux-amd64.tar.gz
 linux-amd64/
 linux-amd64/README.md
 linux-amd64/helm
 linux-amd64/LICENSE
 
>_ ll
 total 303M
 drwxrwxr-x 11 danesh danesh 4.0K Oct 11 11:27 fzf
 drwxrwxr-x  9 danesh danesh 4.0K Nov  6 19:01 google-cloud-sdk
 -rw-rw-r--  1 danesh danesh  13M Oct 26 10:37 helm-v3.4.0-linux-amd64.tar.gz
 drwxr-xr-x  2 danesh danesh 4.0K Oct 26 10:36 linux-amd64
 -rwxrwxr-x  1 danesh danesh  54M Nov  6 18:10 minikube
 -rwxr-xr-x  1 danesh danesh 119M Sep 30 12:55 packer
 -rwxr-xr-x  1 danesh danesh  82M Sep 30 13:10 terraform
 -rwxr-xr-x  1 danesh danesh  37M Aug 24 18:02 vagrant

 >_ cp linux-amd64/helm .

 >_ rm -rfv linux-amd64
 >_ rm helm-v3.4.0-linux-amd64.tar.gz

 >_ ll
 total 330M
 drwxrwxr-x 11 danesh danesh 4.0K Oct 11 11:27 fzf
 drwxrwxr-x  9 danesh danesh 4.0K Nov  6 19:01 google-cloud-sdk
 -rwxr-xr-x  1 danesh danesh  40M Nov  6 19:42 helm
 -rwxrwxr-x  1 danesh danesh  54M Nov  6 18:10 minikube
 -rwxr-xr-x  1 danesh danesh 119M Sep 30 12:55 packer
 -rwxr-xr-x  1 danesh danesh  82M Sep 30 13:10 terraform
 -rwxr-xr-x  1 danesh danesh  37M Aug 24 18:02 vagrant

>_ helm version
 version.BuildInfo{Version:"v3.4.0", GitCommit:"7090a89efc8a18f3d8178bf47d2462450349a004", GitTreeState:"clean", GoVersion:"go1.14.10"}
```