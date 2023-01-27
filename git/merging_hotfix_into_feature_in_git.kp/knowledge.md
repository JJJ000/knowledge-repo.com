---
title: Combine the hotfix branch into the feature branch using git merge
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To merge a hotfix branch into a feature branch, use the command `git merge hotfix-branch-name feature-branch-name`.
---

**Contents**

[TOC]

### Step 1: Checkout Feature Branch

In your local repository, you need to checkout the feature branch where you want to merge the hotfix branch.

```
git checkout <feature-branch>
```

### Step 2: Merge Hotfix Branch

Once you are in the feature branch, you can now merge the hotfix branch.

```
git merge <hotfix-branch>
```

### Step 3: Resolve Conflicts

If there are any conflicts between the two branches, you need to resolve them before you can commit the changes.

### Step 4: Push Changes

Once the conflicts are resolved, you can now push the changes to the remote repository.

```
git push origin <feature-branch>
```
