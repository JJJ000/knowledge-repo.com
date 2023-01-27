---
title: What is the difference between a local git branch and its remote branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run the command `git diff <local branch> <remote branch>` to compare a local Git branch with its remote branch.
---

**Contents**

[TOC]

### Step 1: Fetch Remote Branch

In order to compare a local Git branch with its remote branch, the first step is to fetch the remote branch. This can be done by running the following command:

```git
git fetch <remote>
```

Where `<remote>` is the name of the remote repository.

### Step 2: Checkout Local Branch

Next, checkout the local branch that you want to compare with its remote branch. This can be done by running the following command:

```git
git checkout <branch>
```

Where `<branch>` is the name of the local branch.

### Step 3: Compare Branches

Finally, to compare the local branch with its remote branch, run the following command:

```git
git diff <remote>/<branch>
```

Where `<remote>` is the name of the remote repository and `<branch>` is the name of the branch. This will show all the differences between the local branch and its remote branch.
