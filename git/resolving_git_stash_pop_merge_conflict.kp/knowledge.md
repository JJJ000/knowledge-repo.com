---
title: Revert the changes made by 'git stash pop' that caused a merge conflict
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Revert the changes with `git reset --hard` before attempting to `git stash pop` again.
---

**Contents**

[TOC]

### Step 1: Revert the Changes

The first step in undoing a `git stash pop` that results in a merge conflict is to revert the changes that were applied by the `stash pop`. This can be done using `git reset HEAD~1`. This command will undo the last commit, which in this case is the commit that was created when the `git stash pop` was performed.

### Step 2: Resolve the Merge Conflict

Once the changes have been reverted, the next step is to resolve the merge conflict. This can be done by manually editing the conflicting files and resolving the conflicts.

### Step 3: Commit the Changes

Once the conflicts have been resolved, the changes need to be committed. This can be done using `git commit -m "Resolved merge conflict"`.

### Step 4: Reapply the Stash

Finally, the stash can be reapplied using `git stash apply`. This will reapply the changes that were stashed prior to the `git stash pop` that caused the merge conflict.
