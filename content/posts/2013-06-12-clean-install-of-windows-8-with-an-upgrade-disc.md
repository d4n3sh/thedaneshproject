---
title: Clean Install of Windows 8 with an Upgrade Disc
author: Danesh
date: 2013-06-13T02:20:29+00:00
dsq_thread_id:
  - 1394290959

---
[<img loading="lazy" alt="windows activation" src="/wp-content/uploads/2013/06/windows-activation-450x239.png" width="450" height="239" />][1]

I lost my hard drive and was trying to install Windows 8 from a Windows USB boot disk. When came time to activate I was greeted with &#8220;Code: 0xC004F061 your key can only be used for an upgrade&#8221;.  I bought the upgrade license during the launch sale but din&#8217;t know about this restriction.

Microsoft&#8217;s solution was to first install Windows 7 and then run the Upgrade assistant again to upgrade to Windows 8.  That would take too long!

Some Googling later and a solution was found. A simple registry hack. Here&#8217;s how,

  1. &#8220;Windows + r &#8221; and type &#8220;regedit&#8221; to bring up the registry.
  2. Navigate to `HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Setup/OOBE/`
  3. Double click on &#8220;MediabootInstall&#8221;
  4. Change the value from &#8220;1&#8221; to &#8220;0&#8221;. Exit the registry.
  5. Hit the &#8220;Windows&#8221; key and search for &#8220;cmd&#8221; . Right click and select &#8220;Run as Administrator&#8221;.
  6. Type `slmgr /rearm` and hit press enter. Wait for confirmation.
  7. Reboot.
  8. Try to active again. Should work now.

Picture Guide below.<!--more-->

[<img loading="lazy" alt="windows activation run regedit" src="/wp-content/uploads/2013/06/windows-activation-run-regedit.png" width="413" height="213" />][2]

[<img loading="lazy" class="alignnone size-medium wp-image-3230" alt="windows activation regedit" src="/wp-content/uploads/2013/06/windows-activation-regedit-450x157.png" width="450" height="157" srcset="/wp-content/uploads/2013/06/windows-activation-regedit-450x157.png 450w, /wp-content/uploads/2013/06/windows-activation-regedit.png 728w" sizes="(max-width: 450px) 100vw, 450px" />][3]

[<img loading="lazy" class="alignnone size-full wp-image-3229" alt="windows activation regedit media boot install" src="/wp-content/uploads/2013/06/windows-activation-regedit-media-boot-install.png" width="345" height="206" />][4]

[<img loading="lazy" class="alignnone size-medium wp-image-3228" alt="windows activation cmd" src="/wp-content/uploads/2013/06/windows-activation-cmd-450x253.png" width="450" height="253" srcset="/wp-content/uploads/2013/06/windows-activation-cmd-450x253.png 450w, /wp-content/uploads/2013/06/windows-activation-cmd-1024x576.png 1024w, /wp-content/uploads/2013/06/windows-activation-cmd.png 1920w" sizes="(max-width: 450px) 100vw, 450px" />][5]

[<img loading="lazy" class="alignnone size-full wp-image-3227" alt="windows activation cmd done" src="/wp-content/uploads/2013/06/windows-activation-cmd-done.png" width="356" height="170" />][6]

&nbsp;

 [1]: /wp-content/uploads/2013/06/windows-activation.png
 [2]: /wp-content/uploads/2013/06/windows-activation-run-regedit.png
 [3]: /wp-content/uploads/2013/06/windows-activation-regedit.png
 [4]: /wp-content/uploads/2013/06/windows-activation-regedit-media-boot-install.png
 [5]: /wp-content/uploads/2013/06/windows-activation-cmd.png
 [6]: /wp-content/uploads/2013/06/windows-activation-cmd-done.png