---
title: What is the process for undoing multiple git commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can revert multiple Git commits by using the `git revert` command with the specific commit hashes.
---

**Contents**

[TOC]

### Reverting with `git revert`

The `git revert` command is used to undo a single commit. It creates a new commit that undoes the changes of the specified commit.

1. Find the commit you want to revert:
   - Use `git log` to find the commit you want to revert.
   - Make note of the commit's SHA-1 hash.

2. Revert the commit:
   - Run `git revert <SHA-1 hash>` to revert the commit.
   - You can also use the `-n` flag to avoid committing the revert.

### Reverting with `git reset`

The `git reset` command is used to undo multiple commits at once. It resets the repository to the specified commit, discarding all commits after it.

1. Find the commit you want to reset to:
   - Use `git log` to find the commit you want to reset to.
   - Make note of the commit's SHA-1 hash.

2. Reset the repository to the specified commit:
   - Run `git reset --hard <SHA-1 hash>` to reset the repository to the specified commit.
   - You can also use the `--soft` flag to keep the changes from the reverted commits.

3. Push the changes:
   - Run `git push --force` to push the changes to the remote repository.
