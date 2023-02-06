---
title: Removing a local branch using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To delete a local branch with Git, use the command `git branch -d <branch\_name>`.
---

**Contents**

[TOC]

## Deleting a Local Branch

1. Checkout to the branch you want to delete: `git checkout <branch_name>`
2. Delete the local branch: `git branch -d <branch_name>`
3. Push the changes to the remote repository: `git push origin --delete <branch_name>`

## Deleting a Remote Branch

1. Fetch the remote branches: `git fetch --all`
2. Delete the remote branch: `git push origin --delete <branch_name>`
