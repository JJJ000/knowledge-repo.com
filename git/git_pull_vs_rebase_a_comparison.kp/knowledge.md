---
title: Comparing git pull and git rebase
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git Pull downloads and merges remote changes into the local repository, while Git Rebase replays local commits on top of remote changes.
---

**Contents**

[TOC]

### Git Pull
Git Pull is a command that retrieves the latest version of a repository from a remote source and integrates it with the local version of the repository. It is a combination of two commands, git fetch, which fetches the latest version of the remote repository and git merge, which merges the changes from the remote repository into the local repository.

### Git Rebase
Git Rebase is a command that takes all the changes from one branch and applies them onto another. It is often used to integrate changes from one branch onto another, such as when updating a feature branch with changes from the master branch. Unlike git pull, git rebase does not merge the branches, but instead applies the changes from one branch onto the other.
