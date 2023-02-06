---
title: What is the distinction between git pull --rebase and git pull --ff-only?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git pull --rebase will attempt to rebase the local branch onto the remote branch, while git pull --ff-only will only fast-forward the local branch if it can be cleanly merged with the remote branch.
---

**Contents**

[TOC]

# Git Pull --Rebase

Git pull --rebase is a combination of git fetch and git rebase. It fetches the specified remote repository and then merges the local branch with the remote branch using rebase. This command is used to keep the local branch up-to-date with the remote branch, while also preserving the local commits.

# Git Pull --FF-Only

Git pull --ff-only is a combination of git fetch and git merge. It fetches the specified remote repository and then merges the local branch with the remote branch using fast-forward merge. This command is used to keep the local branch up-to-date with the remote branch, while also discarding any local commits that are not present in the remote branch.

# Difference

The primary difference between git pull --rebase and git pull --ff-only is that git pull --rebase preserves the local commits, while git pull --ff-only discards any local commits that are not present in the remote branch. Additionally, git pull --rebase will create a new commit for each local commit that is preserved, whereas git pull --ff-only will not create any new commits.
