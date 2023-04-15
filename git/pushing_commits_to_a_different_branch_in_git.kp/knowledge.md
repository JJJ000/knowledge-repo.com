---
title: Submit changes to a different branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To push commits to another branch in Git, use the command `git push <remote> <branch>`.
---

**Contents**

[TOC]

### Push to Another Branch

### Step 1: Checkout the Target Branch

To push commits to another branch, the first step is to checkout the target branch. This can be done using the `git checkout` command, followed by the name of the branch you want to switch to:

```
git checkout <target-branch>
```

### Step 2: Pull from the Target Branch

Before pushing to the target branch, it is important to pull any changes that have been made since the last time you pulled. This can be done using the `git pull` command:

```
git pull
```

### Step 3: Push to the Target Branch

Once the target branch has been checked out and any changes have been pulled, the commits can be pushed to the target branch using the `git push` command:

```
git push origin <target-branch>
```

### Step 4: Check the Status

Finally, it is important to check the status of the push to make sure that the commits have been successfully pushed to the target branch. This can be done using the `git status` command:

```
git status
```
