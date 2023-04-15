---
title: What is the process for performing a "git pull" without applying local changes?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `--force` flag to overwrite local changes when pulling with git.
---

**Contents**

[TOC]

### Step 1: Stash Local Changes

Before attempting to pull from a remote repository, you must first ensure that any local changes you have made are safely stashed away. This can be done by running the following command:

```git
git stash
```

### Step 2: Pull from Remote Repository

Once your local changes have been stashed, you can then proceed to pull from the remote repository. This can be done by running the following command:

```git
git pull
```

### Step 3: Pop Stashed Changes

After the pull has been completed, you can then pop the stashed changes back onto your local branch. This can be done by running the following command:

```git
git stash pop
```

### Step 4: Resolve Merge Conflicts (If Necessary)

If there are any conflicts between the local changes and the changes pulled from the remote repository, you will need to resolve them before continuing. This can be done by using a merge tool such as `git mergetool`.
