---
title: What is the difference in commits between the master branch and the specified branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The number of commits ahead/behind master is the difference between the number of commits on master and the number of commits on the branch.
---

**Contents**

[TOC]

### Git Ahead/Behind Info

Git ahead/behind info is a way to measure the divergence between two branches in a Git repository. It is calculated by comparing the two branches and determining the number of commits that are in one branch but not the other.

### Master vs. Branch

When comparing the master branch to another branch, the git ahead/behind info will tell you how many commits are in the master branch that are not in the other branch (the "ahead" number) and how many commits are in the other branch that are not in the master branch (the "behind" number).

### Merging Branches

If the ahead and behind numbers are both zero, then the branches are in sync and no commits need to be merged. If the ahead number is greater than zero, then the other branch needs to be updated with the commits in the master branch. If the behind number is greater than zero, then the master branch needs to be updated with the commits in the other branch.

### Resolving Conflicts

If the ahead and behind numbers are both greater than zero, then the branches have diverged and there may be conflicts that need to be resolved. In this case, the commits from both branches need to be merged together to create a unified version of the code.
