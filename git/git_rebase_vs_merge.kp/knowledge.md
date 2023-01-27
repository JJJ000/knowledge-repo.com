---
title: What are the differences between using git rebase and git merge?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Git rebase is used when you want to keep a linear history, whereas Git merge is used when you want to maintain the branching history.
---

**Contents**

[TOC]

#When to Use Git Rebase

1. When You Want a Cleaner History
Git rebase can be used to create a cleaner history when merging branches. This is because it allows you to combine multiple commits into one, eliminating unnecessary merge commits. This can be especially helpful when working with a shared repository as it allows for a more concise and readable history.

2. When You Want to Keep Your Feature Branch Up to Date
Git rebase can be used to keep your feature branch up to date with the master branch. This is done by replaying your feature branch commits on top of the master branch. This ensures that your feature branch is always up to date with the latest changes in the master branch.

#When to Use Git Merge

1. When You Want to Preserve the History
Git merge can be used to preserve the history of a branch. When merging two branches, the commits from both branches are preserved in the resulting merge commit. This allows for a more detailed view of the history of the project.

2. When You Want to Keep Your Feature Branch Separate
Git merge can be used to keep your feature branch separate from the master branch. This is done by creating a new merge commit that combines the commits from both branches. This allows you to keep your feature branch separate while still having access to the latest changes in the master branch.
