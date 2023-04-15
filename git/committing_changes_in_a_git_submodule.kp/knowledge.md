---
title: What is the process for saving changes in a git submodule?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To commit changes in a git submodule, use the git submodule foreach command.
---

**Contents**

[TOC]

### Adding Changes

1. Change into the directory of the submodule and make the desired changes.
2. Add the changed files to the staging area with `git add <file>`.
3. Commit the changes with `git commit -m "<message>"`.

### Pushing Changes

1. Push the changes to the submodule's remote repository with `git push <remote> <branch>`.

### Updating Parent Repository

1. Change into the parent repository and add the submodule's changes with `git add <submodule path>`.
2. Commit the changes with `git commit -m "<message>"`.

### Pushing Changes to Parent Repository

1. Push the changes to the parent repository's remote repository with `git push <remote> <branch>`.
