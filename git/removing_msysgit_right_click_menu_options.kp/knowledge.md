---
title: What is the process for getting rid of the right click menu options in msysgit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Right-click on the msysgit icon in the system tray and select `Exit`.
---

**Contents**

[TOC]

1. Uninstall msysgit

To remove the right click menu options associated with msysgit, the program must be uninstalled.

2. Remove Registry Keys

msysgit adds registry keys to the Windows registry, which can be removed to prevent the right click menu options from appearing. The registry keys are located in the following location: 

`HKEY_CLASSES_ROOT\Directory\Background\shell\Git`

3. Clear Context Menu

To ensure that the right click menu options are completely removed, the context menu must be cleared. This can be done by running the following command in an elevated command prompt: 

`reg delete "HKEY_CLASSES_ROOT\Directory\Background\shell\Git" /f`

4. Reboot

Finally, the computer must be rebooted in order for the changes to take effect.
