---
title: Does the git-merge command have a dry-run option?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: No, there is no git-merge --dry-run option.
---

**Contents**

[TOC]

### No

Git does not have a `git-merge --dry-run` option.

### Why

The purpose of a `--dry-run` option is to simulate the effects of a particular command without actually executing it. This is useful for testing changes before making them permanent.

However, in the case of `git-merge`, there is no way to simulate the effects of a merge without actually performing the merge. This is because a merge involves combining the changes from two different branches, and there is no way to simulate this without actually performing the merge.

### Alternatives

Although there is no `git-merge --dry-run` option, there are several alternatives that can be used to simulate the effects of a merge.

The first option is to use the `git-diff` command to compare the differences between the two branches before performing the merge. This will allow you to see what changes will be made before actually performing the merge.

Another option is to use the `git-stash` command to temporarily store the changes from one branch before performing the merge. This will allow you to test the changes from one branch without actually merging them into the other branch.

Finally, you can use the `git-checkout` command to switch between branches without performing a merge. This will allow you to test the changes from one branch without merging them into the other branch.
