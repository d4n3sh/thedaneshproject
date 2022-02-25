---
title: Changing my permalinks structure
author: Danesh Manoharan
date: 2007-08-19T18:55:56+00:00
pvc_views:
  - 2099
dsq_thread_id:
  - 889736660

---
I decided to change my permalinks structure to no longer include %category% as part the url. I was thinking about long term maintenance and noticed a possible flaw in the current structure which is /category/post/. What happens if I decide to remove or rename a category? My url structure would change and break all incoming links. This is not a good experience for my readers.

I made the change transparent and this is how I did it.

Changed my permalinks structure through _**WP-Admin->Options->Permalinks**_ to reflect the new structure shown below.

Old structure : _**/%category%/%postname%/**_

New structure : _**/posts/%postname%/**_

[![permalink structure][1]][2]

What happens to all the incoming links from other sites? Fixed that by using the [permalink-redirect][3] plug in by [Scott Yang][4]. See screenshot below.

[<img src="/wp-content/uploads/2007/08/permalink-redirect.jpg" title="permalink redirect" alt="permalink redirect" width="500" />][5]

The plug in was initially installed to help add a trailing slash "/" to all my posts url(s) and also redirect all www.thedaneshproject.com to thedaneshproject.com. This was to help improve the accuracy of traffic tracking through [Google Analytics][6] and [Google Webmaster][7]. Now it is playing a larger role by making my permalink changes transparent to all incoming links which may be pointing to my old structure. A sample of what it is doing,

"/voip/major-skype-outage/" will now point to "/posts/major-skype-outage/"

That's it, now I'll have to wait and if anything broke.

If you need any help applying the same changes to your WP blog please leave a comment or get in touch with me though the [Contact Me][8] form and I'll be glad to help.

 [1]: /wp-content/uploads/2007/08/permalink-structure.jpg
 [2]: /wp-content/uploads/2007/08/permalink-structure.jpg "permalink structure"
 [3]: http://fucoder.com/code/permalink-redirect/
 [4]: http://scott.yang.id.au/
 [5]: /wp-content/uploads/2007/08/permalink-redirect.jpg "permalink redirect"
 [6]: http://www.google.com/url?sa=t&ct=res&cd=1&url=http%3A%2F%2Fwww.google.com%2Fanalytics%2F&ei=X4zIRrXoM5COgAPl7bDPBg&usg=AFQjCNFz3Lrd3h9xlat60IUur_H8rmADdw&sig2=ZXTu2Sb2qxBUXQztQD0f5Q
 [7]: http://www.google.com/url?sa=t&ct=res&cd=1&url=http%3A%2F%2Fwww.google.com%2Fwebmasters%2F&ei=c4zIRsKtBpXWgQOo8vXoBg&usg=AFQjCNHRdsvJbOWLCqMoLtM0kUyTiNOzdw&sig2=W4zAuqv-I55JYnfEIWrsUA
 [8]: /contact-me/