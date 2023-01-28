---
title: Shortcut for pushing the current branch to git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The shortcut for pushing the current branch is `git push origin HEAD`.
---

**Contents**

[TOC]

### Command

`git push -u origin HEAD`

### Description

This command will push the current branch to the remote repository. The `-u` flag sets the upstream configuration so that the current branch will track the remote branch. The `origin` argument specifies the remote repository and `HEAD` specifies the current branch.

### Examples

To push the current branch to the remote repository `origin`:

```git
git push -u origin HEAD
```

### Additional Resources

* [Git Reference - git-push](https://git-scm.com/docs/git-push)
