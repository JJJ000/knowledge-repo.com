---
title: What is the best way to combine a git branch into the master branch without any issues?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git merge <branch\_name>` while on the master branch to safely merge the specified branch into master.
---

**Contents**

[TOC]

### 1. Create a New Branch

Before merging a branch into master, it is important to create a new branch from master. This ensures that the master branch remains untouched and the changes can be tested in the new branch before merging.

### 2. Commit & Push Changes

Once the new branch is created, any changes should be committed and pushed to the remote repository. This allows for the changes to be tested and reviewed by other team members before merging.

### 3. Merge the Branch

Once all changes are committed and pushed, the branch can be merged into master. This can be done using the `git merge` command, or through a pull request on GitHub.

### 4. Resolve Conflicts

When merging branches, conflicts may arise. It is important to resolve any conflicts before merging the branch into master. This can be done using the `git mergetool` command or manually editing the conflicting files.
