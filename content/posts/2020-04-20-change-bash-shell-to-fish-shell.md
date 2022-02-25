---
title: Change BASH shell to FISH shell
author: Danesh Manoharan
date: 2020-04-20T10:25:59+00:00
draft: false
---
I used the change shell command _**chsh**_ to change the default shell environment for my id from [BASH][1] to the [FISH][2] shell.

```bash
>_ chsh 
Changing shell for danesh.manoharan. 
New shell [/bin/bash]: /usr/bin/fish 
Password: 
Shell changed. 

>_ chsh -s /usr/bin/fish 
Changing shell for danesh.manoharan. 
chsh: Shell changed. 
```

 [1]: https://www.gnu.org/software/bash/
 [2]: https://fishshell.com/
