---
title: Remove the OBS virtual webcam device on Mac
author: Danesh
date: 2021-06-23T02:44:23+00:00
featured_image: /wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img4.png
advanced_seo_description:
  - Remove the OBS virtual webcam device on Mac
draft: false
---
The OBS virtual webcam device doesn't always get removed properly when OBS studion is removed on Mac. Here's how to manually remove the device.

  1. Using finder navigate to "/Library/CoreMediaIO/ Plug-Ins/DAL/".  
    `Command + Shift + g` will bring up the goto dialog.  
<img loading="lazy" width="497" height="214" class="wp-image-8427" style="width: 400px;" src="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img3.png" alt="goto dialog" srcset="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img3.png 497w, /wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img3-450x194.png 450w" sizes="(max-width: 497px) 100vw, 497px" />  
    
  2. Delete the "obs-mac-virtualcam.plugin" file.  
<img loading="lazy" width="859" height="248" class="wp-image-8428" style="width: 450px;" src="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img2.png" alt="remove file" srcset="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img2.png 859w, /wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img2-450x130.png 450w, /wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img2-768x222.png 768w" sizes="(max-width: 859px) 100vw, 859px" />  
    
  3. Verify if the "obs-virtual-camera" device has been removed.  
    The screenshot below is from MS Teams.  
{{< figure src="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img1.png" link="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img1.png" alt="webcam list in MS Teams" width=450 position="center" >}}
