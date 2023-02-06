---
title: What is the command to display a combined diff output for a merge commit, even when all files are the same as one of the parents?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the command `git show -m --first-parent <merge\_commit>`.
---

**Contents**

[TOC]

# Section 1: What is a Merge Commit?
A merge commit is a type of commit that combines two or more separate branches of development into a single branch. It is created when a user merges two branches together. The merge commit contains the changes from both branches and a message that explains the merge.

# Section 2: What is "git show"?
Git show is a command used to display the contents of a commit. It displays the commit message, the changes that were made, and the author of the commit.

# Section 3: How to "git show" a Merge Commit
To show a merge commit, use the following command:

`git show <merge commit hash>`

This will show the merge commit message, the changes that were made, and the authors of the commit.

# Section 4: How to "git show" a Merge Commit with Combined Diff Output
To show a merge commit with combined diff output, use the following command:

`git show --cc <merge commit hash>`

This will show the merge commit message, the changes that were made, and the authors of the commit, as well as a combined diff output of the changes. This is useful when every changed file agrees with one of the parents.
