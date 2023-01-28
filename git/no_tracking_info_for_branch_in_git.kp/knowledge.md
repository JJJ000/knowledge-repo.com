---
title: No records of the present branch can be found
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Git does not track changes made to the current branch.
---

**Contents**

[TOC]

### What is Tracking Information?
Tracking information in Git is a way to keep track of the relationship between a local branch and a remote branch. This allows users to easily fetch and push changes to the remote branch, as well as keep the local branch up to date with the remote branch.

### How to Check for Tracking Information
To check for tracking information, users can use the `git branch -vv` command. This command will list all local branches and their associated remote branches, if any.

### What if There is No Tracking Information?
If there is no tracking information for a branch, then the branch is not associated with a remote branch. This means that the branch will not be able to fetch or push changes to the remote branch.

### How to Set Up Tracking Information
In order to set up tracking information, users can use the `git branch --set-upstream-to` command. This command will associate the local branch with the specified remote branch.
