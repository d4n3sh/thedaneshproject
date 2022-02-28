---
title: History command with time stamp
author: Danesh Manoharan
date: 2010-02-08T05:44:23+00:00
pvc_views:
  - 5967
dsq_thread_id:
  - 889819319

---
Running the ' history ' command only gives you line numbers. Sometimes it's useful to have a time stamp attached to each command to build a clearer picture.

Simply set the " HISTTIMEFORMAT " env variable to enable time stamps in ' history '.

Run the command below.

`export HISTTIMEFORMAT=' %F %T '`

Before:

![](/wp-content/uploads/2010/02/history.timestamp.1-450x393.png)

After:

![](/wp-content/uploads/2010/02/history.timestamp.2-450x393.png)