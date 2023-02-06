---
title: There is an index.lock file that appears when I attempt to commit, but I am unable to delete it
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `git fsck` command to check for any issues with the repository, then delete the index.lock file.
---

**Contents**

[TOC]

# Solution 1: Using the Terminal
1. Open the Terminal.
2. Navigate to the directory containing the `index.lock` file.
3. Type `rm index.lock` and press enter.

# Solution 2: Using File Explorer
1. Open the File Explorer.
2. Navigate to the directory containing the `index.lock` file.
3. Right-click on the `index.lock` file and select "Delete".
