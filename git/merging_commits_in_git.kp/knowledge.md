---
title: What is the process for combining a particular commit from one branch into another branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To merge a specific commit from one branch into another, use the git cherry-pick command.
---

**Contents**

[TOC]

## Step 1: Checkout the Branch

Check out the branch you want to merge the commit into.

```
git checkout <target_branch>
```

## Step 2: Fetch the Remote Branch

Fetch the remote branch in order to get the commit you want to merge.

```
git fetch origin <source_branch>
```

## Step 3: Merge the Commit

Merge the commit you want to merge from the source branch into the target branch.

```
git merge <source_branch> <commit_hash>
```

## Step 4: Push the Changes

Push the changes to the remote branch.

```
git push origin <target_branch>
```
