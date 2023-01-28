---
title: Change to a different branch and discard any modifications without saving them
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use `git checkout -f <branch\_name>` to switch branches and ignore any changes without committing.
---

**Contents**

[TOC]

### Stash Uncommitted Changes

Git provides a command to temporarily store uncommitted changes in order to switch branches without committing them. This command is `git stash`.

### Switch Branches

Once the uncommitted changes have been stashed, you can switch branches with the `git checkout` command. 

### Reapply Stashed Changes

Once you have switched to the desired branch, you can reapply the stashed changes with the `git stash pop` command. This will apply the changes to the current branch.

### Clean Up

Finally, you can clean up any remaining stashed changes with the `git stash drop` command. This will remove the stashed changes from the list of stashed changes.
