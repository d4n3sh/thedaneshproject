---
title: WordPress is_home() conditional tag
author: Danesh Manoharan
date: 2008-08-14T09:04:11+00:00
robotsmeta:
  - index,follow
pvc_views:
  - 16865
dsq_thread_id:
  - 890612061

---
![](/wp-content/uploads/2008/08/wordpresslogo.jpg)

I use the **is_home()** conditional tag to control when my ads show up. I prefer to only have my ads show up when single posts are viewed. Helps keep my home page looking clean and relevant.

Currently, I have my ads setup to show on all pages except for my home page. To get the same functionality setup on your WordPress simply wrap your ad codes with the code below.  
`<br />
<?php if ( !( is_home() ) ) { ?>`

[your ad codes go here.... ]

<?php } ?>

ALternatively if you want your ads to only show up on your home page,

`<?php if (Ã‚Â  is_home()Ã‚Â  ) { ?>`

[your ad codes go here.... ]

<?php } ?>

If you use static pages for your home instead, then **replace is_home()** with **is\_front\_page()** .

Try it out, drop me a note if you need help.

 [1]: /wp-content/uploads/2008/08/wordpresslogo.jpg)