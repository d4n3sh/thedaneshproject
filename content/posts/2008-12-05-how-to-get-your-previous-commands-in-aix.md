---
title: How to get your previous commands in AIX
author: Danesh Manoharan
date: 2008-12-05T01:45:52+00:00
pvc_views:
  - 6238
robotsmeta:
  - index,follow
dsq_thread_id:
  - 889856044

---
Without an auto complete feature like in BASH, AIX appears more complicated then it really is. Especially amongst new users.The retyping of commands can get real annoying sometimes.

Fortunately, accessing your command history is easyly acomplished in AIX and will save you a load of time.

To start off, run "`set -o vi`" to set the shell to "_VI_" or "_Insert Mode_" mode.

`[akuny][/users/jabas] # set -o vi`

Next, hit the "Esc" key to get into VI mode. Once in vi mode follow the combinations below to scroll through your command history.

**Alt + <k>**key to go back

**Alt + <j>** key to go forward

Alternatively you could;

**Alt + <->**key to go back

**Alt + <+>**key to go forward

Enjoy.