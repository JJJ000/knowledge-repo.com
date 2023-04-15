---
title: What is the process for selectively incorporating changes from another branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the `git cherry-pick <commit>` command to selectively merge or pick changes from another branch.
---

**Contents**

[TOC]

### Using Git Merge

1. Checkout the branch you want to merge changes into.
2. Use `git merge` with the `--no-commit` option to review the changes that will be merged:

```git
git merge --no-commit <other-branch>
```

3. Use `git diff` to review the changes that will be merged.
4. Use `git reset HEAD` to unstage the changes.
5. Use `git add -p` to selectively stage the changes you want to keep.
6. Once you have staged the changes you want to keep, use `git commit` to commit the merge.

### Using Git Rebase

1. Checkout the branch you want to merge changes into.
2. Use `git rebase` with the `--interactive` option to review the changes that will be merged:

```git
git rebase --interactive <other-branch>
```

3. Use `git diff` to review the changes that will be merged.
4. Use `git reset HEAD` to unstage the changes.
5. Use `git add -p` to selectively stage the changes you want to keep.
6. Once you have staged the changes you want to keep, use `git rebase --continue` to continue the rebase.
7. Once the rebase is complete, use `git rebase --abort` to abort the rebase.
