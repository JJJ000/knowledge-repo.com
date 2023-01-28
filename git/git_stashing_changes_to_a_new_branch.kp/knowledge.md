---
title: How do the changes stored in git stash apply to a new branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: No, stashed changes will not be applied to a new branch.
---

**Contents**

[TOC]

### Yes

Stashing changes allows you to switch branches without losing your changes. When you switch branches, the changes you have stashed are applied to the new branch.

### How

To stash changes and apply them to a new branch, you can use the `git stash` command. This command will save your changes and then apply them to the new branch when you switch.

### Example

For example, if you have changes in your current branch and you want to switch to a new branch, you can use the following commands:

```git
git stash
git checkout <new_branch>
git stash pop
```

The first command saves your changes, the second command switches to the new branch, and the third command applies the changes you stashed to the new branch.
