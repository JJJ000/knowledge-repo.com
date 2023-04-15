---
title: How can I un-track a remote branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To stop tracking a remote branch in Git, use the command `git branch --unset-upstream`.
---

**Contents**

[TOC]

### Delete the Remote Branch
1. Fetch the latest changes from the remote repository: `git fetch`
2. Delete the remote branch: `git push origin --delete <branch_name>`

### Stop Tracking Locally
1. Check out the local branch you want to stop tracking: `git checkout <branch_name>`
2. Unset the upstream branch for the local branch: `git branch --unset-upstream`
