---
title: What is the process for removing unpushed git commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can delete unpushed git commits by using the `git reset` command with the `--hard` option.
---

**Contents**

[TOC]

### Reset to a Previous Commit
1. Checkout the commit you want to reset to using `git checkout <commit_hash>`
2. Run `git reset --hard` to reset the branch to that commit

### Remove Unpushed Commits
1. Checkout the branch with the commits you want to delete using `git checkout <branch_name>`
2. Run `git reset --hard HEAD~<number_of_commits>` to delete the commits
3. Push the branch to the remote repository with `git push -f origin <branch_name>`
