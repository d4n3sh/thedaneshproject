---
title: Installing KIND on Ubuntu 20.10
author: Danesh
date: 2020-11-11T02:19:36+00:00
url: /posts/installing-kind-on-ubuntu-20-10/

---
KIND == Kubernetes in Docker

I will install the KIND binary into my ~/bin/ directory since that&#8217;s where I keep all my binaries.

<pre class="wp-block-code"><code>>_ cd ~/.bin
 
>_ curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.9.0/kind-linux-amd64
   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                  Dload  Upload   Total   Spent    Left  Speed
 100    97  100    97    0     0    163      0 --:--:-- --:--:-- --:--:--   162
 100   642  100   642    0     0    831      0 --:--:-- --:--:-- --:--:--   831
 100 7247k  100 7247k    0     0  4742k      0  0:00:01  0:00:01 --:--:-- 18.6M
 >_ chmod +x kind

 >_ which kind
 /home/danesh/.bin/kind

 >_ kind version
 kind v0.9.0 go1.15.2 linux/amd64

>_ source &lt;(kind completion zsh)</code></pre>