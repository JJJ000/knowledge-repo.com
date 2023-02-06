---
title: What steps must be taken to create a 'open git-bash here...' option in the windows explorer context menu?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Right-click on the Windows Explorer background and select `Git Bash Here` from the context menu.
---

**Contents**

[TOC]

1. Prerequisites
---
- Windows 10
- Git Bash

2. Create a Shortcut
---
1. Right-click on the Desktop and select **New** > **Shortcut**.
2. In the **Type the location of the item** field, type the following:

`C:\Program Files\Git\git-bash.exe`

3. Click **Next**.
4. Type a name for the shortcut, such as **Git Bash**, and click **Finish**.

3. Add the Shortcut to the Context Menu
---
1. Right-click on the Desktop and select **New** > **Text Document**.
2. Name the file **GitBashHere.reg** and open it in Notepad.
3. Copy and paste the following code into the file:

```
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\shell\gitbash]
@="Git Bash Here"
"Icon"="C:\\Program Files\\Git\\git-bash.exe"

[HKEY_CLASSES_ROOT\Directory\shell\gitbash\command]
@="C:\\Program Files\\Git\\git-bash.exe"
```

4. Save the file and double-click it to add the shortcut to the registry.

4. Test the Shortcut
---
1. Right-click on any folder in Windows Explorer and select **Git Bash Here**.
2. Git Bash should open in the selected folder.
