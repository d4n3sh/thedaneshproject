---
title: Select all files but one on linux
author: Danesh
date: 2008-01-10T02:00:29+00:00
url: /posts/select-all-files-but-one-on-linux/
pvc_views:
  - 4175
dsq_thread_id:
  - 890004881

---
My friend wanted to know how to select all files but one on the CLI or in a bash script. This is how I normally do it, do you know a better way?  
**  
_From the command line_**

    ls * | grep -v [pattern to ignore]

or

    ls [!pattern to ignore]  *

in a bash script it may look like this,

    
    for i in `ls * | grep -v [pattern to ignore]`
    do
       do something here
    done
    

<!--more-->

  
![][1]

 [1]: http://img72.imageshack.us/img72/9606/ignorebi8.png