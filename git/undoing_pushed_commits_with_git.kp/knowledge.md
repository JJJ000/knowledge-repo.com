---
title: What is the process for reverting pushed commits using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can undo pushed commits using git by reverting the commits or using the git revert command.
---

**Contents**

[TOC]

### Revert Commits

The `git revert` command can be used to undo commits that have already been pushed to a remote repository. This command creates a new commit that undoes the changes of the specified commit, while preserving the project history.

### Reset Commits

The `git reset` command can also be used to undo commits that have already been pushed to a remote repository. This command removes the specified commits from the project history, and can be used to "undo" multiple commits at once. Note that this command should be used with caution, as it permanently removes commits from the project history.

### Rebase Commits

The `git rebase` command can be used to undo commits that have already been pushed to a remote repository. This command rewrites the project history, allowing you to move, edit, or delete commits. This can be used to "undo" multiple commits at once, while preserving the project history.

### Revert and Push

Once you have undone the commits using one of the above methods, you can then push the changes to the remote repository using the `git push` command. This will update the remote repository with the new commits, effectively undoing the original commits.
