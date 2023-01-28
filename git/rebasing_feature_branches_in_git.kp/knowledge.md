---
title: Merge the feature branch onto another feature branch using rebase
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To rebase a feature branch onto another feature branch in Git, use the command `git rebase <other-branch-name>`.
---

**Contents**

[TOC]

### Step 1: Fetch the Feature Branches

The first step is to fetch the feature branches from the remote repository. This can be done by running the following command:

```
git fetch origin <feature-branch-1> <feature-branch-2>
```

### Step 2: Checkout the Desired Feature Branch

Once the feature branches have been fetched, the desired feature branch can be checked out by running the following command:

```
git checkout <feature-branch-2>
```

### Step 3: Rebase the Feature Branch

Once the desired feature branch has been checked out, the feature branch can be rebased onto the other feature branch by running the following command:

```
git rebase <feature-branch-1>
```

### Step 4: Push the Feature Branch

Finally, the rebased feature branch can be pushed to the remote repository by running the following command:

```
git push origin <feature-branch-2>
```
