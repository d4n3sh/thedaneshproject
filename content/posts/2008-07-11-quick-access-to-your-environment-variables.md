---
title: quick access to your environment variables
author: Danesh
date: 2008-07-11T06:54:20+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 1755
dsq_thread_id:
  - 900011390

---
Here's a quick way to access your environment variables from the CLI.

User the "%" key in conjunction with your "<tab>" key to auto complete your environment variables.

`pandora:/ # echo $J <TAB><br />
$JAVA_BINDIRÃ‚Â  $JAVA_HOMEÃ‚Â Ã‚Â Ã‚Â  $JAVA_ROOTÃ‚Â Ã‚Â Ã‚Â  $JDK_HOMEÃ‚Â Ã‚Â Ã‚Â Ã‚Â  $JRE_HOME<br />
pandora:/ # echo $JAVA_ <TAB><br />
$JAVA_BINDIRÃ‚Â  $JAVA_HOMEÃ‚Â Ã‚Â Ã‚Â  $JAVA_ROOT<br />
pandora:/ # echo $JAVA_HOME<br />
/usr/lib/jvm/java`

The traditional way is to "`env | grep [variable name]`"