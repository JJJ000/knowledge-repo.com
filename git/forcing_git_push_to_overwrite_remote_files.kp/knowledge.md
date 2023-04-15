---
title: Override remote files with a git push
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: No, it is not possible to force git push to overwrite remote files.
---

**Contents**

[TOC]

### Force Push

Git push can be forced to overwrite remote files using the `--force` or `-f` flag. This flag tells Git to force the push, even if it results in a non-fast-forward merge.

### Syntax

The syntax for forcing a push is:

```git
git push <remote> <branch> --force
```

Where `<remote>` is the name of the remote repository and `<branch>` is the name of the branch you are pushing to.

### Warning

It is important to note that forcing a push can cause data loss if other users have pushed changes to the same branch. Therefore, it should only be used in cases where you are certain that no other users have pushed changes to the same branch.

### Alternatives

If you want to keep your local changes and the remote changes, you can use `git pull` to merge the remote changes with your local changes. This will result in a fast-forward merge that does not require the `--force` flag.
