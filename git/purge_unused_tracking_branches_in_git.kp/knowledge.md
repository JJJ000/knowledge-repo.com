---
title: Delete local tracking branches that are no longer on the remote
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git fetch -p` to prune any tracking branches that are no longer on the remote.
---

**Contents**

[TOC]

### Remove Tracking Branches Locally

1. List all the local branches: `git branch -v`
2. Identify the tracking branches that are no longer on remote: `git branch -vv`
3. Remove the local tracking branches: `git branch -d <branch_name>`

### Remove Tracking Branches Remotely

1. List all the remote branches: `git branch -r`
2. Identify the tracking branches that are no longer on remote: `git branch -vv`
3. Remove the remote tracking branches: `git push origin --delete <branch_name>`
