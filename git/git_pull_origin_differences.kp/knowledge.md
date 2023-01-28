---
title: The difference between 'git pull origin master' and 'git pull origin/master' is that the former will fetch the specified branch from the remote repository and merge it with the local branch, while the latter will fetch the specified branch from the local repository and merge it with the local branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git pull origin master pulls the specified branch from the remote repository and merges it with the local branch, whereas git pull origin/master pulls the specified branch from the local repository.
---

**Contents**

[TOC]

### Git Pull Origin Master

Git pull origin master is a command that fetches the branch from the remote repository and merges it with the local branch. It is used to update the local branch with the changes from the remote repository.

### Git Pull Origin/Master

Git pull origin/master is a command that fetches the branch from the remote repository and merges it with the local branch. However, the difference between this command and git pull origin master is that it does not create a local branch, but instead updates the local branch with the changes from the remote repository.
