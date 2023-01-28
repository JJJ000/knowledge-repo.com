---
title: What are the differences between two commits without any commits in between?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git diff` command with the commit hashes of the two commits to view the changes.
---

**Contents**

[TOC]

### Using Git Diff

Git diff is a useful command for seeing the changes between two commits. It can be used to compare the differences between two commits without commits in-between. To do this, you can use the following command:

`git diff <commit1> <commit2>`

This will show you the differences between the two commits, without any commits in-between.

### Using Git Log

Git log is another useful command for seeing the changes between two commits. It can be used to compare the differences between two commits without commits in-between. To do this, you can use the following command:

`git log --oneline --graph --decorate --all`

This will show you a graph of the commits, with the differences between the two commits highlighted.

### Using Git Show

Git show is a useful command for seeing the changes between two commits. It can be used to compare the differences between two commits without commits in-between. To do this, you can use the following command:

`git show <commit1>..<commit2>`

This will show you the differences between the two commits, without any commits in-between.

### Using Git Blame

Git blame is a useful command for seeing the changes between two commits. It can be used to compare the differences between two commits without commits in-between. To do this, you can use the following command:

`git blame <commit1>..<commit2>`

This will show you the changes between the two commits, without any commits in-between.
