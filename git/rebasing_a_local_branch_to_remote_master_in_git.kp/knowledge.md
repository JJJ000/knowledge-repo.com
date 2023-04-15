---
title: What steps do I need to take to rebase my local branch onto the remote master branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git rebase origin/master` to rebase the local branch onto the remote master.
---

**Contents**

[TOC]

#1 Cloning the Remote Repo

Before rebasing a local branch onto the remote master, you will need to clone the remote repository. This can be done by running the following command:

`git clone <remote-repo-url>`

#2 Checking Out the Local Branch

Once the remote repository is cloned, you will need to check out the local branch that you want to rebase onto the remote master. This can be done by running the following command:

`git checkout <local-branch-name>`

#3 Rebasing the Local Branch

Now that you have the local branch checked out, you can rebase it onto the remote master. This can be done by running the following command:

`git rebase origin/master`

#4 Pushing the Changes

After the local branch has been rebased onto the remote master, you will need to push the changes. This can be done by running the following command:

`git push -f origin <local-branch-name>`
