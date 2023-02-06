---
title: What is the process for deleting a particular version from the git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git revert` command to remove a specific revision from the git history.
---

**Contents**

[TOC]

**1. Using git revert**

Git revert can be used to remove a specific revision in the git history. This command creates a new commit that undoes the changes of the specified commit.

**2. Steps to Revert a Commit**

- Check out the branch that contains the commit you want to revert.
- Use the git log command to list the commits in the branch.
- Find the commit you want to revert and copy its SHA-1 hash.
- Use the git revert command with the SHA-1 hash of the commit you want to revert.

**3. Using git reset**

Git reset can also be used to remove a specific revision in the git history. This command resets the current branch head to the specified commit and removes any commits after it.

**4. Steps to Reset a Commit**

- Check out the branch that contains the commit you want to reset.
- Use the git log command to list the commits in the branch.
- Find the commit you want to reset and copy its SHA-1 hash.
- Use the git reset command with the SHA-1 hash of the commit you want to reset.
