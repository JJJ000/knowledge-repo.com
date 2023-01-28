---
title: Combine all changes from another branch into a single commit, discarding all intermediate commits
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To merge all changes from another branch as a single commit in Git, use the `--squash` flag when merging.
---

**Contents**

[TOC]

### Step 1: Checkout the Target Branch

First, you need to checkout the target branch you want to merge changes from. This can be done with the following command:

```
git checkout <target-branch>
```

### Step 2: Merge the Source Branch

Next, you need to merge the source branch into the target branch. This can be done with the following command:

```
git merge --squash <source-branch>
```

### Step 3: Commit the Changes

Finally, you need to commit the changes with a single commit. This can be done with the following command:

```
git commit -m "<commit-message>"
```

### Step 4: Push the Changes

Once the changes have been committed, you can push the changes to the remote repository with the following command:

```
git push origin <target-branch>
```
