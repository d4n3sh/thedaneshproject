---
title: Extract ZIP files in Linux
author: Danesh
date: 2007-09-05T17:12:59+00:00
pvc_views:
  - 35901
dsq_thread_id:
  - 889737421

---
ZIP archives are most commonly used in Windows/MS-DOS based environments.

In Linux, you can use the &#8220;unzip&#8221; command to extract,list or test ZIP files. Below are the common tasks I use &#8220;unzip&#8221; for.

Extract the contents of a ZIP file into it&#8217;s own directory and also create subdirectories as needed.

> \# unzip [filename].zip

Extract the contents of a ZIP file into the current directory only. No subdirectories will be created.

> \# unzip -j [filename].zip

Extract the contents of a ZIp file into a custom directory.

> \# unzip -d \[target directory\] \[filename\].zip

List the contents of a ZIP file.

> \# unzip -l [filename].zip

Test the integrity of a ZIP file and it&#8217;s contents.

> Ã‚Â # unzip -t [filename].zip
> 
> \# unzip -tq [filename].zip (Only shows summary)

Extract the contents of a ZIP file only if the files already exist in the target directory. Good for upgrades.

> \# unzip -f [filename].zip
> 
> \# unzip -fo [filename].zip (non interactive. Yes to all)

Extract the contents of a ZIP file if the contents are newer then what&#8217;s available in the target directory or don&#8217;t exist yet. Good for upgrades.

> \# unzip -u [filename].zip
> 
> \# unzip -uo [filename].zip (non interactive. Yes to all)

Did this help? If you need further information please drop me a comment.