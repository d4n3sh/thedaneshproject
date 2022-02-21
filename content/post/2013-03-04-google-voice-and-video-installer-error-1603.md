---
title: Google voice and video installer error 1603
author: Danesh
date: 2013-03-04T09:16:21+00:00
dsq_thread_id:
  - 1116265137

---
[<img loading="lazy" class="alignnone size-medium wp-image-3132" alt="Google Voice Error 1603" src="/wp-content/uploads/2013/03/Google-voice-and-video-chat-Installer_2013-03-02_11-22-32-450x155.png" width="450" height="155" srcset="/wp-content/uploads/2013/03/Google-voice-and-video-chat-Installer_2013-03-02_11-22-32-450x155.png 450w, /wp-content/uploads/2013/03/Google-voice-and-video-chat-Installer_2013-03-02_11-22-32.png 456w" sizes="(max-width: 450px) 100vw, 450px" />][1]

&nbsp;

For some stupid reason my Google hangout and voice calls stopped working on my Windows machine. Removed the Google voice plugin and tried reinstalling it and got hit with a new error &#8220;Installer error 1603&#8221;.

After some digging around the issue was narrowed down to either permissions or the windows installer service having some hangover files or registry entries from previous installs.

The fix was to run Window&#8217;s FixIt to clean up the installer. This is what it does;

  * Removes bad registry key on 64 bit operating systems.
  * Windows registry keys that control the upgrade (patching) data that become corrupted.
  * Resolves problems that prevent new programs from being installed.
  * Resolves problems that prevent programs from being completely uninstalled and blocking new installations and updates.
  * Use this troubleshooter for an uninstall only if the program fails to uninstall using the windows add/remove programs feature.

&nbsp;

<a title="Microsoft FixIt" href="http://support.microsoft.com/mats/Program_Install_and_Uninstall/" target="_blank" rel="noopener">Download Here</a>

[<img loading="lazy" class="alignnone size-full wp-image-3133" alt="microsoft_fix_it_small" src="/wp-content/uploads/2013/03/microsoft_fix_it_small.png" width="300" height="169" />][2]

&nbsp;

Let me know if it work for you.

 [1]: /wp-content/uploads/2013/03/Google-voice-and-video-chat-Installer_2013-03-02_11-22-32.png
 [2]: http://support.microsoft.com/mats/Program_Install_and_Uninstall/