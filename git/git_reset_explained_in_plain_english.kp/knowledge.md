---
title: Git reset is a command that reverts changes to a file or files in a git repository back to a previous version
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git reset is a command that will reset the current branch head to a previous commit.
---

**Contents**

[TOC]

### Overview

Git reset is a command used to reset changes in a Git repository. It can be used to reset the working directory to a particular commit, undo local changes, or discard commits in the local repository. 

### Reset Working Directory

Git reset can be used to reset the working directory to a particular commit. This is done by specifying the commit hash or a tag. This will reset the working directory to the state of the specified commit, and all changes made since then will be discarded.

### Undo Local Changes

Git reset can also be used to undo local changes. This is done by specifying the "--hard" flag when running the command. This will discard all changes made since the last commit and reset the working directory to the state of the last commit.

### Discard Commits

Git reset can also be used to discard commits in the local repository. This is done by specifying the "--hard" flag and the commit hash or tag of the commit you want to reset to. This will discard all commits made since the specified commit and reset the working directory to the state of the specified commit.
