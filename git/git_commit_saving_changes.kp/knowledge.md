---
title: What is preventing my changes from being saved when I use 'git commit'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git commit only saves changes that have been staged with `git add` first.
---

**Contents**

[TOC]

# Overview

Git commit is an important part of the version control system that allows developers to save changes to their code. However, if a commit is not done correctly, the changes may not be saved.

# What is Git Commit?

Git commit is a command that is used to save changes to a project in the version control system Git. When a commit is made, a snapshot of the current state of the project is taken and stored in the project's history. This allows developers to track changes and revert back to previous versions of the project if needed.

# Why Commit May Not Save Changes

There are several reasons why a commit may not save changes. The most common reason is that the commit was not done correctly. This could be due to forgetting to add files to the commit, not staging changes, or not entering a commit message. Another reason could be that the changes were made to a file that is not tracked by Git.

# How to Avoid This

To avoid this issue, it is important to make sure that all changes are added to the commit and that the commit message is clear and descriptive. Additionally, all files that need to be tracked by Git should be added to the repository. Finally, it is important to double-check the commit to make sure that all changes are included before pushing it to the remote repository.
