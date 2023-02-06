---
title: How can I merge my 'detached head' commits into the master branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git merge` command to merge the detached HEAD commits back into master.
---

**Contents**

[TOC]

# Section 1: Checking the Current Status

Before attempting to merge detached HEAD commits back into the master branch, it is important to check the current status of the repository. This can be done by running the `git status` command, which will show the current branch, the commits that have been made, and any changes that have been made to the repository.

# Section 2: Merging the Detached HEAD

Once the current status of the repository has been determined, the next step is to merge the detached HEAD commits back into the master branch. This can be done by running the `git merge` command, with the detached HEAD as the target. This will merge the commits from the detached HEAD into the master branch.

# Section 3: Resolving Conflicts

When merging a detached HEAD into the master branch, it is possible that conflicts may arise. If this happens, it is important to resolve the conflicts before continuing. This can be done by running the `git mergetool` command, which will open a graphical user interface that can be used to resolve the conflicts.

# Section 4: Pushing Changes

Once the conflicts have been resolved and the detached HEAD has been merged into the master branch, the final step is to push the changes to the remote repository. This can be done by running the `git push` command, which will push the changes to the remote repository.
