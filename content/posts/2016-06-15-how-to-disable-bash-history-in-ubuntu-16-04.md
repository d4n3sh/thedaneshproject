---
title: How to disable bash history in Ubuntu 16.04
author: Danesh Manoharan
date: 2016-06-15T05:16:04+00:00
dsq_thread_id:
  - 4911357169

---
Append either line below to the end of your .bashrc file, start a new bash terminal and history should now be turned off.

<pre class="toolbar:2 lang:default decode:true">shopt -u -o history
</pre>

<span style="line-height: 1.5;">or</span>

<pre class="toolbar:2 lang:default decode:true">set +o history
</pre>

<span style="line-height: 1.5;">Don't forget </span><span style="line-height: 1.5;">clear</span><span style="line-height: 1.5;"> out the old history file too.</span>

<pre class="toolbar:2 lang:default decode:true"># history -c;</pre>

 