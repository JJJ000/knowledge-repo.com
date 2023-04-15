---
title: What is the best way to view the results of a merge in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use `git diff <branch1> <branch2>` to preview a merge.
---

**Contents**

[TOC]

### Using Git Diff

Git diff allows you to compare two different versions of a file or two different branches. This can be used to preview a merge. To do this, use the following command:

`git diff <source_branch> <target_branch>`

This will show you the differences between the two branches, allowing you to preview the merge.

### Using Git Log

Git log allows you to view the commit history of a file or branch. This can be used to preview a merge. To do this, use the following command:

`git log --oneline --decorate --graph --all`

This will show you the commit history of all branches, allowing you to view the changes that will be merged.

### Using Git Merge Tool

Git merge tool allows you to view the changes that will be made when merging two branches. This can be used to preview a merge. To do this, use the following command:

`git mergetool <source_branch> <target_branch>`

This will open a graphical user interface which will show you the changes that will be made when merging the two branches.
