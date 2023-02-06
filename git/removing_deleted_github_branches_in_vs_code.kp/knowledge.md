---
title: How do I get rid of branches that have been deleted on github but still appear in visual studio code?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In VS Code, you can use the Source Control view to delete any local branches that were deleted on GitHub.
---

**Contents**

[TOC]

# Solution 1:
1. Open the Command Palette (Ctrl + Shift + P)
2. Type in `Git: Prune`
3. Press enter

# Solution 2:
1. Open the Command Palette (Ctrl + Shift + P)
2. Type in `Git: Fetch`
3. Press enter
4. Type in `Git: Prune`
5. Press enter
