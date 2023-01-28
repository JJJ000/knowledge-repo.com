---
title: Reverting the remote to a specific commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To reset a remote to a certain commit in Git, use the command `git reset --hard <commit-hash>`.
---

**Contents**

[TOC]

#1 Resetting a Commit

1. Check out the commit you want to reset to: `git checkout <commit-hash>`

2. Create a new branch from the commit: `git checkout -b <new-branch-name>`

3. Reset the remote branch to the commit: `git push --force <remote-name> <new-branch-name>`

#2 Resetting the Working Directory

1. Check out the commit you want to reset to: `git checkout <commit-hash>`

2. Reset the working directory to the commit: `git reset --hard`

#3 Resetting the Staging Area

1. Check out the commit you want to reset to: `git checkout <commit-hash>`

2. Reset the staging area to the commit: `git reset --mixed`

#4 Resetting the Index

1. Check out the commit you want to reset to: `git checkout <commit-hash>`

2. Reset the index to the commit: `git reset --soft`
