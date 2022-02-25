---
title: Remove the OBS virtual webcam device on Mac
author: Danesh Manoharan
date: 2021-06-23T02:44:23+00:00
featured_image: /wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img4.png
advanced_seo_description:
  - Remove the OBS virtual webcam device on Mac
draft: false
---
The OBS virtual webcam device doesn't always get removed properly when OBS studion is removed on Mac. Here's how to manually remove the device.

1. Using finder navigate to "/Library/CoreMediaIO/ Plug-Ins/DAL/".
`Command + Shift + g` will bring up the goto dialog.  
{{< figure src="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img3.png" alt="goto dialog" align="left" >}}  

2. Delete the "obs-mac-virtualcam.plugin" file.
{{< figure src="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img2.png" alt="remove file" align="left" >}}  

3. Verify if the "obs-virtual-camera" device has been removed.
The screenshot below is from MS Teams.  
{{< figure src="/wp-content/uploads/2021/06/remove-the-obs-virtual-webcam-device-on-mac-img1.png" alt="webcam list in MS Teams" align="left" >}}
