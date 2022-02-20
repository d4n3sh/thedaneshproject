---
title: Installing Franz on Arch Linux
author: Danesh
date: 2017-03-07T14:49:35+00:00
url: /posts/installing-franz-on-arch-linux/
dsq_thread_id:
  - 5610625987

---
<figure id="attachment_3822" aria-describedby="caption-attachment-3822" style="width: 450px" class="wp-caption alignnone"><img loading="lazy" class="size-medium wp-image-3822" src="/wp-content/uploads/2017/03/franz-450x336.png" alt="Franz" width="450" height="336" srcset="/wp-content/uploads/2017/03/franz-450x336.png 450w, /wp-content/uploads/2017/03/franz-768x574.png 768w, /wp-content/uploads/2017/03/franz-1024x765.png 1024w, /wp-content/uploads/2017/03/franz.png 1362w" sizes="(max-width: 450px) 100vw, 450px" /><figcaption id="caption-attachment-3822" class="wp-caption-text">Franz</figcaption></figure>

[Franz][1] is a new multi-platform messaging app for Linux, MAC and Windows. Been running it my Arch boxes for a few months now and am loving it!

It&#8217;s not in the default repo so you&#8217;ll need the AUR to install it. [ArchWiki][2]

Once you have your AUR setup, pull the package down and build it.

<pre class="lang:sh decode:true ">~&gt;$ yaourt -Sy franz-bin</pre>

 [1]: http://meetfranz.com/
 [2]: https://wiki.archlinux.org/index.php/Arch_User_Repository