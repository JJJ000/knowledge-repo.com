---
title: Can you explain the purpose of the 'git restore' command and how it differs from 'git reset'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The `git restore` command restores files in the working tree that have been deleted or modified, while `git reset` resets the current branch head to a specified state.
---

**Contents**

[TOC]

#### Git Restore

Git Restore is a command used to restore changes made to a file that have been staged, but not yet committed. It can be used to undo changes to a file that have been added to the staging area, but not yet committed to the repository.

#### Git Reset

Git Reset is a command used to reset the state of a repository to a specified commit. It can be used to undo commits and reset the repository to a previous state.

#### Difference

The main difference between Git Restore and Git Reset is that Git Restore is used to undo changes to files that have been added to the staging area, while Git Reset is used to undo commits and reset the repository to a previous state. Additionally, Git Restore does not affect the repository, while Git Reset does.
