---
title: Add only the modified changes to git and ignore any untracked files
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: `git add -u`
---

**Contents**

[TOC]

1. **Git Add All Modified Changes**

To add all modified changes, run the following command:

```git
git add -A
```

This will add all modified and untracked files to the staging area.

2. **Git Add Only Modified Changes**

To add only modified changes, run the following command:

```git
git add -u
```

This will add only modified files to the staging area and will ignore untracked files.

3. **Git Add Only Untracked Files**

To add only untracked files, run the following command:

```git
git add .
```

This will add only untracked files to the staging area and will ignore modified files.

4. **Git Add Specific Changes**

To add specific changes, run the following command:

```git
git add <file>
```

This will add only the specified file to the staging area and will ignore all other modified and untracked files.
