---
title: Redoing a git merge commit by changing the base commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: It is not possible to rebase a Git merge commit.
---

**Contents**

[TOC]

# Section 1: What is a Merge Commit?
A merge commit is a commit that merges two or more branches together. It is created when a user merges two branches together in their Git repository. The merge commit contains all the changes from both branches and is used to combine the two branches into one.

# Section 2: What is Rebasing?
Rebasing is the process of taking a series of commits and reapplying them onto a different branch. It is used to move commits from one branch to another while preserving the original commit history. 

# Section 3: Rebase a Merge Commit
Rebasing a merge commit is a bit more complicated than a regular commit. The process involves first finding the merge commit and then using the `git rebase` command to move the merge commit onto the desired branch. The process is as follows:

1. Find the merge commit. This can be done by using the `git log` command and searching for the merge commit.
2. Use the `git rebase` command to move the merge commit onto the desired branch.
3. Resolve any merge conflicts that may arise.
4. Once the conflicts are resolved, use the `git rebase --continue` command to finish the rebase process.

# Section 4: Conclusion
Rebasing a merge commit is a bit more complicated than rebasing a regular commit, but it is still possible to do. With the right commands and a bit of patience, it is possible to move a merge commit onto a different branch while preserving the original commit history.
