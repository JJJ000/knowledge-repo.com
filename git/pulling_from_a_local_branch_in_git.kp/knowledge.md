---
title: How to merge changes from a local branch into another one?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To `pull` from a local branch into another one in Git, use the command `git pull <source> <destination>`.
---

**Contents**

[TOC]

### Step 1: Checkout the Source Branch

First, you need to checkout the source branch that you want to pull from. This can be done by running the following command:

```
git checkout <source_branch_name>
```

### Step 2: Pull from the Source Branch

Next, you need to pull from the source branch that you just checked out. This can be done by running the following command:

```
git pull <source_branch_name>
```

### Step 3: Checkout the Target Branch

Now, you need to checkout the target branch that you want to pull into. This can be done by running the following command:

```
git checkout <target_branch_name>
```

### Step 4: Merge the Source Branch into the Target Branch

Finally, you need to merge the source branch into the target branch. This can be done by running the following command:

```
git merge <source_branch_name>
```
