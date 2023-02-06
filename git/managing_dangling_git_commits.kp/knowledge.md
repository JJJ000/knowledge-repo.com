---
title: Identifying and removing git commits that are not associated with any branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To list dangling commits, use the command `git fsck --no-reflog --unreachable`; to delete them, use the command `git prune`.
---

**Contents**

[TOC]

### Listing Dangling Commits

1. Run the command `git fsck --no-reflog | grep commit` to list out all commits that are not associated with any branch.

2. This command will output a list of all dangling commits in the form of a SHA-1 hash.

### Deleting Dangling Commits

1. To delete a dangling commit, use the command `git reset --hard <SHA-1 hash>`. 

2. This command will delete the commit with the corresponding SHA-1 hash.

3. If you want to delete all dangling commits, you can use the command `git fsck --unreachable --no-reflog | grep commit | cut -d" " -f3 | xargs git reset --hard`.
