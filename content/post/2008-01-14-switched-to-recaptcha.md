---
title: Switched to reCAPTCHA
author: Danesh
date: 2008-01-14T15:41:10+00:00
url: /posts/switched-to-recaptcha/
pvc_views:
  - 3382
dsq_thread_id:
  - 916599114

---
<img loading="lazy" src="http://farm3.static.flickr.com/2055/2191989334_8441734778_o.png" height="201" width="362" />

Switched over from [Math Comment Spam Protection][1] to [reCAPTCHA][2]. Spam has still been coming in despite the Math Comment Spam Protection plugin. I decided to take reCAPTCHA for a spin for a few weeks. Hopefully it helps.

_**What is reCAPTCHA?**_

You need a CAPTCHA differentiate human from computers. There are many other CAPTCHA programs available today, from numbers to whole phrases. Almost every website with registration, comments or basically any sort of forms implement some kind of CAPTCHA to keep spam bots at bay.

I chose reCAPTHA because it&#8217;s CAPTCHA function not only stops spam but also helps in the digitizing of books from the [internet archive][3]. It does this by adding OCR unrecognized words into it&#8217;s CAPTCHA images for users to solve. Sometimes the CAPTCHA gets pretty scrambled and can be hard to read. To aid users an additional word gets added to the CAPTCHA image which has been previously solved. A user normally only needs to get the solved word correct, the unrecognized word will be compared against answers from other users and the most accurate one then gets picked.

You can get the reCAPTCHA WordPress plugin here.

Source: [reCAPTCHA][4]

 [1]: http://sw-guide.de/wordpress/plugins/math-comment-spam-protection/
 [2]: http://recaptcha.net/
 [3]: http://www.archive.org/
 [4]: http://recaptcha.net