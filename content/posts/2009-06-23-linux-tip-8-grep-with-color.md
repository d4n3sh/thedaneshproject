---
title: 'Linux Tip #8: grep with color'
author: Danesh Manoharan
date: 2009-06-23T00:00:23+00:00
aktt_notify_twitter:
  - no
pvc_views:
  - 3914
dsq_thread_id:
  - 896207632

---
![](/wp-content/uploads/2009/06/grep-with-color-1-500x168.png)

If you're running grep on a large file with multipled results, highlighting your results would really easy on your eyes.

Here's how;

Export the "GREP_OPTIONS" environment variable to include "-color=auto". Run the export command below.

`export GREP_OPTIONS='--color=auto'`

Once you've executed the command, run a simple grep to see the highlights in action.

Red is the default highlight color. I'll cover setting custom colors in a future post.

 [1]: /wp-content/uploads/2009/06/grep-with-color-1.png)