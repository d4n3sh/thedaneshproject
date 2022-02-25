---
title: How to install Linux UVC driver on openSUSE11
author: Danesh
date: 2008-06-26T15:54:55+00:00
pvc_views:
  - 16385
dsq_thread_id:
  - 889966894

---
I recently purchased a webcam for skype. I'm using the [UVC driver][1] to power the webcam on my openSUSE11 machine.

Getting the webcam up was simple with openSUSE.

Verify if the uvc package is available.

`pandora:~ # zypper se uvc<br />
Reading installed packages...`  
`<br />
S | NameÃ‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  | SummaryÃ‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  | Type<br />
--+----------------------+-------------------------------------+-----------<br />
| luvcviewÃ‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  | WebCam viewerÃ‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  | package<br />
| uvcvideoÃ‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â Ã‚Â  | USB Video Class (UVC) webcam driver | srcpackage<br />
| uvcvideo-kmp-debugÃ‚Â Ã‚Â  | USB Video Class (UVC) webcam driver | package<br />
| uvcvideo-kmp-default | USB Video Class (UVC) webcam driver | package<br />
| uvcvideo-kmp-paeÃ‚Â Ã‚Â Ã‚Â Ã‚Â  | USB Video Class (UVC) webcam driver | package<br />
| uvcvideo-kmp-xenÃ‚Â Ã‚Â Ã‚Â Ã‚Â  | USB Video Class (UVC) webcam driver | package<br />
`  
Select the suitable driver for your kernel. " uname -r ". In my case pae.

`pandora:~ # zypper in uvcvideo-kmp-pae<br />
Reading installed packages...`

`The following NEW package is going to be installed:<br />
uvcvideo-kmp-pae</p>
<p>Overall download size: 36.0 K. After the operation, additional 81.0 K will be used.<br />
Continue? [YES/no]: y<br />
Downloading package uvcvideo-kmp-pae-r200_2.6.25.5_1.1-2.2.i586 (1/1), 36.0 K (81.0 K unpacked)<br />
Downloading: uvcvideo-kmp-pae-r200_2.6.25.5_1.1-2.2.i586.rpm [done (6.1 K/s)]<br />
Installing: uvcvideo-kmp-pae-r200_2.6.25.5_1.1-2.2 [done]`

If you want a webcam viewer then install the luvcview package.

`pandora:~ # zypper in luvcview<br />
Reading installed packages...`

`The following NEW package is going to be installed:<br />
luvcview</p>
<p>Overall download size: 45.0 K. After the operation, additional 83.0 K will be used.<br />
Continue? [YES/no]: y<br />
Downloading package luvcview-0.2.4-0.pm.1.i586 (1/1), 45.0 K (83.0 K unpacked)<br />
Downloading: luvcview-0.2.4-0.pm.1.i586.rpm [done (3.2 K/s)]<br />
Installing: luvcview-0.2.4-0.pm.1 [done]<br />
`  
Plug in your webcam and test.

`pandora:~ # luvcview`

 [1]: http://linux-uvc.berlios.de/