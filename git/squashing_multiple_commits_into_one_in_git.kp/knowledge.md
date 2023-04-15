---
title: How can I combine multiple commits into a single squashed commit on another branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the `git rebase -i` command to squash multiple commits into one commit on another branch.
---

**Contents**

[TOC]

### Step 1: Checkout the Target Branch

First, checkout the branch that you want to merge your commits onto.

```
git checkout <target_branch>
```

### Step 2: Rebase the Source Branch onto the Target Branch

Next, rebase the source branch onto the target branch. This will replay all the commits from the source branch onto the target branch.

```
git rebase <source_branch>
```

### Step 3: Squash Commits

Now, squash all the commits from the source branch into a single commit.

```
git rebase -i HEAD~<num_of_commits>
```

This will open an interactive editor window, where you can set all the commits to the "squash" action.

### Step 4: Force Push

Finally, force push the changes to the target branch.

```
git push -f
```
