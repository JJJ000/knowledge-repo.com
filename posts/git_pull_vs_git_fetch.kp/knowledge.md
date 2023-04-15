---
title: What is the difference between the commands `git pull` and `git fetch`?
authors:
- nanja_dev
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The main difference between the two is that `git pull` automatically merges the new data into the current branch, while `git fetch` downloads the new data but does not automatically merge it.
---

**Contents**

[TOC]

### Purpose

* `git pull` is used to download new data and integrate it into the current local repository.
* `git fetch` is used to download new data from a remote repository, but it does not integrate the data into the current local repository.

### Merging

* `git pull` automatically merges the new data into the current branch.
* `git fetch` does not automatically merge the new data into the current branch.

### Use cases

* `git pull` is useful when you want to quickly download and merge new data from a remote repository.
* `git fetch` is useful when you want to review the changes that have been made before deciding whether or not to merge them into your current branch. It is also useful when you want to download new data but keep your current repository unchanged.
