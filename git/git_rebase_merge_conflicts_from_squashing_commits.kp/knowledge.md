---
title: What causes git-rebase to produce merge conflicts when i'm only attempting to squash commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git-rebase can give merge conflicts when squashing commits because it is changing the commit history and can cause conflicts with existing commits.
---

**Contents**

[TOC]

# Overview

Git rebase is a powerful tool that can be used to alter the history of a repository. It can be used to combine multiple commits into one, or to rearrange the order of commits. When using git-rebase to squash commits, it is possible to encounter merge conflicts.

# Causes of Merge Conflicts

Merge conflicts can occur when squashing commits with git-rebase because the changes made in one commit conflict with the changes made in another commit. For example, if one commit changes a certain line of code, and another commit changes the same line of code, a merge conflict will occur.

# Avoiding Merge Conflicts

Merge conflicts can be avoided by carefully reviewing the commits that are being squashed, and ensuring that the changes made in each commit do not conflict with each other. If there is a conflict, it should be resolved before the commits are squashed.

# Conclusion

In conclusion, merge conflicts can occur when squashing commits with git-rebase if the changes made in one commit conflict with the changes made in another commit. To avoid merge conflicts, it is important to carefully review the commits and resolve any conflicts before attempting to squash them.
