---
title: Merging while excluding certain commits from git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can use the `--no-commit` option with git merge to skip specific commits.
---

**Contents**

[TOC]

### 1. Use the `--no-commit` Option

The `--no-commit` option can be used when merging two branches to prevent specific commits from being included in the merge. This option allows you to selectively merge in the commits of one branch while ignoring any commits that you do not want to include. 

### 2. Use `git cherry-pick` 

Another option is to use the `git cherry-pick` command. This command allows you to pick specific commits from one branch and apply them to another. This allows you to select the exact commits that you want to merge while ignoring any commits that you do not want to include. 

### 3. Use `git rebase` 

The `git rebase` command can also be used to selectively merge commits from one branch to another. This command allows you to choose which commits to include in the merge and which commits to ignore. 

### 4. Use `git merge --squash`

Finally, the `git merge --squash` command can be used to squash all of the commits from one branch into a single commit when merging. This allows you to merge all of the changes from one branch without including any of the individual commits.
