---
title: What is the difference between 'assume-unchanged' and 'skip-worktree' in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: `assume-unchanged` marks a file as unchanged to Git, while `skip-worktree` tells Git to ignore local changes in a file.
---

**Contents**

[TOC]

### Assume-Unchanged

The `assume-unchanged` flag is used to mark a file path to be "assumed" as unchanged. This means that Git will not check the file path for any changes and will not include it in the output of `git status`.

### Skip-Worktree

The `skip-worktree` flag is used to mark a file path to be "skipped" when it is checked out. This means that the file path will not be updated when the branch is changed. This is useful for files that should not be changed, such as configuration files.
