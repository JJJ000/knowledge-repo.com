---
title: Revert a commit from the history
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git reset --hard <commit-hash>` command to remove a commit from the history.
---

**Contents**

[TOC]

# Section 1: Revert the Commit

The most straightforward way to remove a commit from the Git history is to use the `git revert` command. This command will create a new commit which reverts the changes introduced by the specified commit. This will effectively remove the commit from the Git history.

# Section 2: Remove the Commit with `git rebase`

Another way to remove a commit from the Git history is to use the `git rebase` command. This command allows you to rewrite the history of a branch by reordering, editing, or deleting commits. This can be used to remove a commit from the history by simply omitting it from the list of commits to be replayed.

# Section 3: Remove the Commit with `git filter-branch`

The `git filter-branch` command can also be used to remove a commit from the Git history. This command allows you to rewrite the history of a branch by filtering out commits based on certain criteria. This can be used to remove a commit from the history by specifying the commit to be filtered out.

# Section 4: Using the `git reset` Command

The `git reset` command can also be used to remove a commit from the Git history. This command allows you to reset the current branch to a specified commit, effectively removing any commits which occurred after the specified commit. This can be used to effectively remove a commit from the Git history.
