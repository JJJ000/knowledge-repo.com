---
title: What are the distinctions between git pull, git fetch, and git rebase?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git pull combines the fetch and rebase commands into one, while git fetch + git rebase fetches remote changes and replays local commits on top of them.
---

**Contents**

[TOC]

**Git Pull**
- Definition: Git pull is a command that downloads the latest version of a remote branch and integrates it with the local branch.

- Process: Git pull fetches the remote branch and directly merges it with the local branch.

**Git Fetch + Git Rebase**
- Definition: Git fetch is a command that downloads the latest version of a remote branch, and git rebase is a command that integrates the remote branch with the local branch.

- Process: Git fetch downloads the remote branch and stores it in the local repository. Git rebase then takes the changes from the remote branch and integrates them with the local branch.
