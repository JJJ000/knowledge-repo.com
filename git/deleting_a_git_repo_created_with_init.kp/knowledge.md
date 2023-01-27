---
title: What is the best way to completely remove a git repository that was initialized?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `rm -rf .git` in the repository directory to fully delete a git repository created with `git init`.
---

**Contents**

[TOC]

### Deleting the Repository
1. Remove the repository from your local machine:  
   `$ rm -rf .git`
2. Remove the repository from the remote server:  
   `$ git push origin :<branch_name>`

### Deleting the Remote Reference
1. Delete the remote reference from your local machine:  
   `$ git remote rm <remote_name>`
2. Delete the remote reference from the server:  
   `$ git push --delete <remote_name> <branch_name>`
