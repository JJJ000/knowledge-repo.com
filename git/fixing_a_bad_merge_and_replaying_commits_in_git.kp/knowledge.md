---
title: What steps can be taken to resolve an unsuccessful merge and reapply the successful commits to the corrected merge?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Revert the bad merge, then cherry-pick the good commits onto the reverted commit.
---

**Contents**

[TOC]

### Step 1: Revert the bad merge

In order to fix the bad merge, the first step is to revert the merge commit. This is done by running the following command:

`git revert <SHA of the merge commit>`

### Step 2: Rebase the good commits

Once the bad merge commit has been reverted, the next step is to rebase the good commits onto the new commit that was created when the bad merge commit was reverted. This is done by running the following command:

`git rebase -i <SHA of the new commit>`

### Step 3: Resolve any conflicts

When rebasing, there may be conflicts that need to be resolved. This is done by manually editing the conflicted files to resolve the conflicts. Once all conflicts are resolved, the changes need to be committed.

### Step 4: Force push to the remote

Once all conflicts have been resolved, the rebase is complete and the changes need to be pushed to the remote. This is done by running the following command:

`git push --force <remote> <branch>`
