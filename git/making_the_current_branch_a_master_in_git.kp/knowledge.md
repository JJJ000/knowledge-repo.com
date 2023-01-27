---
title: Convert the current git branch to a master branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You cannot directly make the current Git branch a master branch; you must create a new master branch and then merge the current branch into it.
---

**Contents**

[TOC]

### Step 1: Checkout the Current Branch

To make the current branch a master branch, the first step is to check out the current branch. This can be done by running the following command:

```git
git checkout <branch-name>
```

Where `<branch-name>` is the name of the current branch.

### Step 2: Create a New Master Branch

Once the current branch is checked out, the next step is to create a new master branch. This can be done by running the following command:

```git
git branch -m master
```

This will create a new master branch from the current branch.

### Step 3: Push the Master Branch

Once the master branch is created, the next step is to push the master branch to the remote repository. This can be done by running the following command:

```git
git push origin master
```

This will push the master branch to the remote repository.

### Step 4: Set the Master Branch as the Default

Finally, to set the master branch as the default branch, the following command can be run:

```git
git branch --set-upstream-to=origin/master master
```

This will set the master branch as the default branch.
