---
title: What happens when you perform a git pull without checking out?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: It is not possible to pull from a Git repository without first checking out a branch.
---

**Contents**

[TOC]

#1 Using Git Fetch

Git fetch is a command that allows you to download objects and refs from a remote repository. It is used to retrieve new work from existing repositories without merging or integrating any of the changes into your local working copy. This makes it possible to pull new changes without checking out any files.

#2 Using Git Merge

Git merge is a command that allows you to combine multiple branches into one. This can be used to pull new changes without checking out any files. With this command, you can merge the remote branch with your local branch and the changes will be applied to your working copy.

#3 Using Git Rebase

Git rebase is a command that allows you to reapply commits on top of an existing branch. This can be used to pull new changes without checking out any files. With this command, you can rebase the remote branch onto your local branch and the changes will be applied to your working copy.

#4 Using Git Cherry-Pick

Git cherry-pick is a command that allows you to selectively apply commits from one branch onto another. This can be used to pull new changes without checking out any files. With this command, you can cherry-pick the commits from the remote branch onto your local branch and the changes will be applied to your working copy.
