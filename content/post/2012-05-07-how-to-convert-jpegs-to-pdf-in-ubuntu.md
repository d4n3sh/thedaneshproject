---
title: How to convert jpegs to pdf in Ubuntu
author: Danesh
date: 2012-05-07T08:37:34+00:00
url: /posts/how-to-convert-jpegs-to-pdf-in-ubuntu/
pvc_views:
  - 3816
dsq_thread_id:
  - 890713445

---
[<img loading="lazy" title="words_to_pdf" src="/wp-content/uploads/2012/05/words_to_pdf.png" alt="" width="405" height="355" />][1]

Had a few documents to scan to PDF urgently today but to my surprise all the cybercafes around my neighborhood didn&#8217;t provide scan to PDF service. The best they could do was scan to jpeg. Hmmm&#8230;why?

Thanks to Linux I had a solution. Scan the docs to jpeg, then convert the jpegs to PDF using imagemagick. Worked like a charm.

Here&#8217;s how, on my Ubuntu 12.04 LTS

Install the imagemagick package if you don&#8217;t already have it.

`:~$ sudo apt-get install imagemagick<br />
`  
Convert a single file.

`:~$ convert scan.jpeg result.pdf<br />
`  
Convert multiple files.

`:~$ convert -adjoin scan*.jpeg result.pdf<br />
`  
or

`:~$ convert -adjoin scan1.jpeg scan2.jpeg result.pdf`

``Did it work for you? Do you have an alternative solution?

 [1]: /wp-content/uploads/2012/05/words_to_pdf.png