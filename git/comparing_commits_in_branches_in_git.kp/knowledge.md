---
title: What commits in one branch are not present in the other?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git log <branch1>..<branch2>` to view the commits in <branch1> that aren`t in <branch2>.
---

**Contents**

[TOC]

# Section 1: Locating the Branches

1. Open the terminal and navigate to the project directory.
2. Run the command `git branch` to view the available branches.

# Section 2: Comparing the Branches

1. Run the command `git log --graph --oneline --decorate --all` to view a graph of the commits in each branch.
2. Compare the commits in the two branches to identify which commits in one branch are not in the other.

# Section 3: Viewing the Commits

1. Run the command `git log --oneline --left-right --graph --cherry-pick --oneline <branch1>...<branch2>` to view the commits that are unique to each branch.
2. The commits on the left side of the output are unique to the first branch, and the commits on the right side are unique to the second branch.

# Section 4: Viewing the Differences

1. To view the differences between the two branches, run the command `git diff <branch1> <branch2>`.
2. This will display the differences between the two branches, including the commits that are unique to each branch.
