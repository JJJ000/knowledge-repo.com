---
title: Is it possible to restore a branch that has been deleted in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Yes, you can recover a deleted branch in Git using the reflog command.
---

**Contents**

[TOC]

### Yes

1. If the branch was recently deleted, you can use the `git reflog` command to view the commit history of the branch.

2. Find the commit ID of the commit before the branch was deleted and use the `git checkout` command with the commit ID to recover the branch.

### No

1. If the branch was deleted long ago, it is not possible to recover it using the `git reflog` command.

2. If the branch has been pushed to a remote repository, it may be possible to recover it from the remote repository.
