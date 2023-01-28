---
title: What is the command to view all remote branches in git 1.7 or higher?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git branch -r` to list all remote branches in Git 1.7+.
---

**Contents**

[TOC]

### Listing Remote Branches

1. Run the command `git branch -r` to list all remote branches.
2. The command will output a list of all remote branches in the current repository.
3. Each branch name will be preceded by the remote name, such as `origin/`, `upstream/`, or `my_remote/`.
4. To list only branches from a specific remote, run `git branch -r <remote_name>`.
