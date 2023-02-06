---
title: Revert some of the unstaged modifications in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use `git reset HEAD <file>` to undo part of unstaged changes in git.
---

**Contents**

[TOC]

### Using git checkout

Git checkout can be used to undo unstaged changes. To do this, use the command `git checkout -- <file>`. This command will discard any changes made to the specified file since the last commit.

### Using git reset

Git reset can also be used to undo unstaged changes. To do this, use the command `git reset HEAD <file>`. This command will reset the specified file to the last commit, discarding any changes made since then.

### Using git revert

Git revert can be used to undo unstaged changes as well. To do this, use the command `git revert HEAD`. This command will create a new commit that reverts the changes made since the last commit.
