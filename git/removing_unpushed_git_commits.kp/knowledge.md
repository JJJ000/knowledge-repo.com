---
title: Revert a git commit which has not been pushed
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the command `git reset --hard HEAD~1` to remove the last commit that has not been pushed.
---

**Contents**

[TOC]

### Option 1: Revert the Commit
1. Checkout the branch you want to remove the commit from.
```
git checkout <branch-name>
```
2. Revert the commit.
```
git revert <commit-hash>
```

### Option 2: Reset the Branch
1. Checkout the branch you want to remove the commit from.
```
git checkout <branch-name>
```
2. Reset the branch to the commit before the unwanted commit.
```
git reset --hard <commit-hash>
```
3. Force push the branch to the remote repository.
```
git push -f
```
