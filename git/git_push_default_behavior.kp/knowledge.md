---
title: What happens when you run "git push" without specifying a branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: By default, git push will push the current branch to its upstream remote branch.
---

**Contents**

[TOC]

### Default Branch

By default, when no branch is specified, the command `git push` will push commits to the current branch.

### Specifying a Remote

If a remote is specified, the command `git push <remote>` will push commits to the branch with the same name as the current branch on the specified remote.

### Specifying a Branch

If a branch is specified, the command `git push <remote> <branch>` will push commits to the specified branch on the specified remote.

### Default Remote

If no remote is specified, the command `git push` will push commits to the branch with the same name as the current branch on the default remote.
