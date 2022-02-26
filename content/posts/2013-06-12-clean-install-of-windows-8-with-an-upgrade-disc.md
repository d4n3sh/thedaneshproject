---
title: Clean Install of Windows 8 with an Upgrade Disc
author: Danesh Manoharan
date: 2013-06-13T02:20:29+00:00
dsq_thread_id:
  - 1394290959

---
![windows activation](/wp-content/uploads/2013/06/windows-activation-450x239.png)

I lost my hard drive and was trying to install Windows 8 from a Windows USB boot disk. When came time to activate I was greeted with "Code: 0xC004F061 your key can only be used for an upgrade".  I bought the upgrade license during the launch sale but din't know about this restriction.

Microsoft's solution was to first install Windows 7 and then run the Upgrade assistant again to upgrade to Windows 8.  That would take too long!

Some Googling later and a solution was found. A simple registry hack. Here's how,

  1. "Windows + r " and type "regedit" to bring up the registry.
  2. Navigate to `HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Setup/OOBE/`
  3. Double click on "MediabootInstall"
  4. Change the value from "1" to "0". Exit the registry.
  5. Hit the "Windows" key and search for "cmd" . Right click and select "Run as Administrator".
  6. Type `slmgr /rearm` and hit press enter. Wait for confirmation.
  7. Reboot.
  8. Try to active again. Should work now.

Picture Guide below.<!--more-->

[![windows activation run regedit](/wp-content/uploads/2013/06/windows-activation-run-regedit.png)
![windows activation regedit](/wp-content/uploads/2013/06/windows-activation-regedit-450x157.png)
![windows activation regedit media boot install](/wp-content/uploads/2013/06/windows-activation-regedit-media-boot-install.png)
![windows activation cmd](/wp-content/uploads/2013/06/windows-activation-cmd-450x253.png)
![windows activation cmd done](/wp-content/uploads/2013/06/windows-activation-cmd-done.png)

 [1]: /wp-content/uploads/2013/06/windows-activation.png
 [2]: /wp-content/uploads/2013/06/windows-activation-run-regedit.png
 [3]: /wp-content/uploads/2013/06/windows-activation-regedit.png
 [4]: /wp-content/uploads/2013/06/windows-activation-regedit-media-boot-install.png
 [5]: /wp-content/uploads/2013/06/windows-activation-cmd.png
 [6]: /wp-content/uploads/2013/06/windows-activation-cmd-done.png
