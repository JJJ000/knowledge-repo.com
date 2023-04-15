---
title: Combine changes up to a specific commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To merge up to a specific commit in Git, use the `git merge` command followed by the commit`s hash.
---

**Contents**

[TOC]

### Step 1: Checkout the branch you want to merge

You need to checkout the branch you want to merge. For example, if you want to merge the `master` branch, you need to run the following command:

```git
git checkout master
```

### Step 2: Pull the latest changes

Once you have checked out the branch, you need to pull the latest changes from the remote repository. To do this, run the following command:

```git
git pull origin master
```

### Step 3: Find the commit you want to merge to

Now, you need to find the commit you want to merge to. To do this, you can use the `git log` command to view the list of commits in the branch.

### Step 4: Merge the branch

Finally, you can merge the branch to the commit you identified in the previous step. To do this, run the following command:

```git
git merge <commit-hash>
```

Where `<commit-hash>` is the hash of the commit you want to merge to.
