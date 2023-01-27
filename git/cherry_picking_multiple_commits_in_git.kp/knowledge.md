---
title: What is the process for selecting multiple commits from a repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To cherry-pick multiple commits in Git, use the `git cherry-pick <commit1> <commit2>...` command.
---

**Contents**

[TOC]

### Clone the Repository

Clone the repository you want to cherry-pick from to your local machine.

### Checkout the Branch

Checkout the branch you want to cherry-pick from.

### Cherry-Pick Commits

Run the command `git cherry-pick <commit-hash>` for each commit you want to cherry-pick.

### Push Changes

Once you have cherry-picked the commits, push the changes to the remote repository.
