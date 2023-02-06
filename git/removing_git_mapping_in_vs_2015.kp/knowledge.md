---
title: Unmap git from visual studio 2015
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Go to the Team Explorer tab, select Settings, choose Git and uncheck the `Enable Git source control provider` option.
---

**Contents**

[TOC]

# Removal Process
1. Open Visual Studio 2015
2. Go to Tools > Options
3. Under the Source Control section, select Plug-in Selection
4. Select "None" from the drop-down menu
5. Click OK

# Confirming Removal
1. Go to File > Source Control
2. If the menu item is no longer available, the git mapping has been successfully removed.
