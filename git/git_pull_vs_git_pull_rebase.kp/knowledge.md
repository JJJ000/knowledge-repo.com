---
title: What is the distinction between git pull and git pull --rebase?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git pull fetches changes from a remote repository and merges them into the local branch, whereas git pull --rebase fetches changes from a remote repository and reapplies them on top of the local branch.
---

**Contents**

[TOC]

### git pull

git pull is a command used to fetch and download content from a remote repository and immediately update the local repository to match that content.

### git pull --rebase

git pull --rebase is similar to git pull, but it is used to ensure that the local branch is up to date with the remote branch before merging the changes. It is used to prevent unnecessary merge commits and keep the history of the project clean. It also ensures that the changes from the remote branch are applied in the correct order, as opposed to the default behavior of git pull which can create merge commits.
