---
title: Display all commits that are present in one branch but not in the other branches using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git log <branch1> ^<branch2>` to show all commits that are in <branch1> but not <branch2>.
---

**Contents**

[TOC]

### Step 1: Fetching Commits

To view all commits that are in one branch, but not the other(s), use the `git log` command with the `--left-right` option. This will compare the current branch with another branch and list the commits that are unique to each branch.

For example, to compare the `master` branch with the `dev` branch, the command would look like this:

`git log --left-right --graph --cherry-pick --oneline master...dev`

### Step 2: Examining the Output

The output of the command will list all commits that are in the `dev` branch, but not in the `master` branch. The commits will be marked with a `<` or `>` symbol, indicating which branch the commit is unique to.

For example, the output might look like this:

```git
< commit 1
> commit 2
< commit 3
> commit 4
```

In this example, `commit 1` and `commit 3` are unique to the `dev` branch, while `commit 2` and `commit 4` are unique to the `master` branch.

### Step 3: Viewing the Commits

To view the details of each commit, use the `git show` command with the commit hash. For example, to view the details of `commit 1`, the command would look like this:

`git show <commit 1 hash>`

### Step 4: Merging the Branches

Once you have identified the commits that are unique to each branch, you can merge the branches together. To do this, use the `git merge` command with the branch name you want to merge into the current branch.

For example, to merge the `dev` branch into the `master` branch, the command would look like this:

`git merge dev`
