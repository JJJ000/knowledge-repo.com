---
title: What is the best way to combine two commits into one if I have already begun rebasing?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the `squash` command while rebasing to combine two commits into one.
---

**Contents**

[TOC]

### Step 1: Abort the Rebase

If you have already started a rebase, the first step is to abort it. To do this, run the following command:

```git
git rebase --abort
```

### Step 2: Rebase the Commits

Once you have aborted the rebase, you can then start the rebase again, but this time with the two commits you want to merge. To do this, run the following command:

```git
git rebase -i <commit-hash>
```

Where `<commit-hash>` is the commit hash of the commit before the two you want to merge.

### Step 3: Squash the Commits

Once the rebase has started, you will be presented with a list of commits. Find the two commits you want to merge and change the action for both of them from `pick` to `squash`.

### Step 4: Continue the Rebase

Once you have made the changes, save the file and exit the editor. Git will then continue the rebase, merging the two commits into one. Once the rebase is complete, you can then push the changes to the remote repository.
