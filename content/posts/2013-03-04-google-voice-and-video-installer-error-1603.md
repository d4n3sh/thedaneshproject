---
title: Google voice and video installer error 1603
author: Danesh Manoharan
date: 2013-03-04T09:16:21+00:00
---
![Google Voice Error 1603](/wp-content/uploads/2013/03/Google-voice-and-video-chat-Installer_2013-03-02_11-22-32-450x155.png)
 

For some stupid reason my Google hangout and voice calls stopped working on my Windows machine. Removed the Google voice plugin and tried reinstalling it and got hit with a new error "Installer error 1603".

After some digging around the issue was narrowed down to either permissions or the windows installer service having some hangover files or registry entries from previous installs.

The fix was to run Window's FixIt to clean up the installer. This is what it does;

  * Removes bad registry key on 64 bit operating systems.
  * Windows registry keys that control the upgrade (patching) data that become corrupted.
  * Resolves problems that prevent new programs from being installed.
  * Resolves problems that prevent programs from being completely uninstalled and blocking new installations and updates.
  * Use this troubleshooter for an uninstall only if the program fails to uninstall using the windows add/remove programs feature.

 

[Download Here](http://support.microsoft.com/mats/Program_Install_and_Uninstall/ "Microsoft FixIt") 

![microsoft_fix_it_small](/wp-content/uploads/2013/03/microsoft_fix_it_small.png)

Let me know if it work for you.

 [1]: /wp-content/uploads/2013/03/Google-voice-and-video-chat-Installer_2013-03-02_11-22-32.png
 [2]: http://support.microsoft.com/mats/Program_Install_and_Uninstall/
