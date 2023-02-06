---
title: Git encountered a fatal error while running in visual studio 2017
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git failed with a fatal error because Visual Studio 2017 does not support Git.
---

**Contents**

[TOC]

# Solution 1:
1. Open the `Team Explorer` tab in Visual Studio.
2. Select the `Settings` option from the `Team Explorer` tab.
3. Select `Git` from the `Settings` menu.
4. Uncheck the `Use Git from Windows Command Prompt` option and click `OK`.

# Solution 2:
1. Open a command prompt window.
2. Navigate to the directory where the project is located.
3. Run the command `git config --global core.autocrlf false` to disable the auto-conversion of line endings.
4. Run the command `git config --global core.longpaths true` to enable long paths.
5. Reopen Visual Studio and try to run the Git commands again.
