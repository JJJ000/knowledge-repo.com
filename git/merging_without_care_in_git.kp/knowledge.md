---
title: I don't mind if the merge process results in the replacement of some untracked working tree files
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the `-f` or `--force` flag to force the merge and overwrite the untracked files.
---

**Contents**

[TOC]

### Force Merge

To force a merge, you can use the `--force` flag. This will cause the merge to happen even if there are untracked working tree files that would be overwritten.

### Discard Local Changes

Another option is to discard any local changes and perform the merge. This can be done by using the `git reset --hard` command. This will reset the working tree to the last commit, discarding any changes that have been made since then.

### Stash Changes

You can also stash any local changes so that they are not overwritten by the merge. This can be done by using the `git stash` command. This will save all of the changes in a temporary area and restore them once the merge is complete.

### Rebase

Finally, you can also perform a rebase instead of a merge. This will apply all of the changes from the branch you are merging into onto the branch you are merging from. This will allow you to keep all of your local changes, but the merge will still be performed.
