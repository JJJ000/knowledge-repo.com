---
title: What is the process for combining two git repositories?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git pull` in one repository to pull in the commits from the other repository.
---

**Contents**

[TOC]

#1 Cloning the Repositories

Clone both of the repositories to your local machine. This can be done with the command `git clone <repository URL>`.

#2 Merging the Repositories

Change the directory to the repository you want to merge into. This can be done with the command `cd <repository name>`.

Merge the other repository into the current repository with the command `git merge <repository name>`.

#3 Resolving Conflicts

If there are any conflicts, resolve them with the command `git mergetool`.

#4 Pushing Changes

Push the changes to the repository with the command `git push`.
