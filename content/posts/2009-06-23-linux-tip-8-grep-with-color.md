---
title: 'Linux Tip #8: grep with color'
author: Danesh
date: 2009-06-23T00:00:23+00:00
aktt_notify_twitter:
  - no
pvc_views:
  - 3914
dsq_thread_id:
  - 896207632

---
[<img loading="lazy" class="alignnone size-medium wp-image-1530" title="grep-with-color-1" src="/wp-content/uploads/2009/06/grep-with-color-1-500x168.png" alt="grep-with-color-1" width="500" height="168" srcset="/wp-content/uploads/2009/06/grep-with-color-1-500x168.png 500w, /wp-content/uploads/2009/06/grep-with-color-1.png 831w" sizes="(max-width: 500px) 100vw, 500px" />][1]

If you're running grep on a large file with multipled results, highlighting your results would really easy on your eyes.

Here's how;

Export the &#8220;GREP_OPTIONS&#8221; environment variable to include &#8220;&#8211;color=auto&#8221;. Run the export command below.

`export GREP_OPTIONS='--color=auto'`

Once you've executed the command, run a simple grep to see the highlights in action.

Red is the default highlight color. I'll cover setting custom colors in a future post.

 [1]: /wp-content/uploads/2009/06/grep-with-color-1.png