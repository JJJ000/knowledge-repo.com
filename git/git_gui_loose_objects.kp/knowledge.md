---
title: What does the git gui mean by 'loose objects'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The `loose objects` that the Git GUI refers to are the individual files, directories, and other objects that are tracked by the Git version control system.
---

**Contents**

[TOC]

#### Unstaged Changes

Unstaged changes are changes to files that have not yet been added to the staging area. These changes are not tracked by Git and will not be included in the next commit.

#### Staged Changes

Staged changes are changes that have been added to the staging area, but have not yet been committed. These changes are tracked by Git and will be included in the next commit.

#### Uncommitted Changes

Uncommitted changes are changes that have been added to the staging area and committed, but have not yet been pushed to the remote repository. These changes are tracked by Git and will be included in the next push.

#### Untracked Files

Untracked files are files that have not yet been added to the staging area. These files are not tracked by Git and will not be included in the next commit.
