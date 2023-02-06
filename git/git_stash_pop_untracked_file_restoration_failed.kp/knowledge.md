---
title: What is the reason that git stash pop is unable to recover untracked files from the stash entry?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git stash pop only restores tracked files, not untracked files.
---

**Contents**

[TOC]

# Overview

Git stash pop is a git command used to restore a stashed change. It will restore the most recent stash entry to the working directory. However, it may not be able to restore untracked files from the stash entry. This is because untracked files are not part of the repository and therefore cannot be restored.

# What are Untracked Files?

Untracked files are files that are not part of the repository. These files are not tracked by git and are not included in the repository. They are also not included in the staged area and will not be committed to the repository.

# Why Can't Git Stash Pop Restore Untracked Files?

Git stash pop cannot restore untracked files because they are not part of the repository. Stash entries are stored in the repository and therefore do not include untracked files. As a result, git stash pop cannot restore untracked files from the stash entry.
