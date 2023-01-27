---
title: What is the process for changing the name of both a local and remote git branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To rename a local and remote branch name, use the git branch -m command to rename the local branch, then use the git push origin old\_branch new\_branch command to update the remote branch.
---

**Contents**

[TOC]

### Rename Local Branch

1. Checkout the local branch you want to rename
   `git checkout <old_branch_name>`
2. Rename the local branch
   `git branch -m <new_branch_name>`

### Rename Remote Branch

1. Push the renamed local branch to the remote repository
   `git push origin <new_branch_name>`
2. Delete the old remote branch
   `git push origin --delete <old_branch_name>`
