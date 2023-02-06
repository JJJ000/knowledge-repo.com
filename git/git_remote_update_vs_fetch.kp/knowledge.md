---
title: What are the distinctions between git remote update and git fetch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git remote update updates the remote tracking branches with the associated remote branches, while git fetch fetches all of the remote references and associated objects.
---

**Contents**

[TOC]

# Git Remote Update
Git remote update is used to update all the remote-tracking branches and the associated objects from a remote repository. It is a combination of git fetch and git prune.

# Git Fetch
Git fetch is used to download objects and refs from another repository. It retrieves the objects and references from the remote repository and stores them in the local repository.

# Differences
1. Git remote update updates all the remote-tracking branches and the associated objects from a remote repository, while git fetch only retrieves the objects and references from the remote repository. 
2. Git remote update is a combination of git fetch and git prune, while git fetch is not. 
3. Git remote update is used to update the local repository with the remote repository, while git fetch is used to download objects and refs from another repository.
