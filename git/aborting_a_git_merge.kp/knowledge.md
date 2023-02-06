---
title: Cancel a git merge
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To abort a Git Merge, use the command `git merge --abort`.
---

**Contents**

[TOC]

## Reset
The simplest way to abort a git merge is to reset the repository to the state before the merge.

## Command
To do this, use the following command:

```
git reset --merge ORIG_HEAD
```

## Explanation
This command will reset the repository to the state before the merge, undoing any changes made during the merge.

## Warning
Be aware that this command will discard any changes made during the merge, so make sure to commit any changes you want to keep before resetting.
