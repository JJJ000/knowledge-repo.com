---
title: Ignore any changes made to files that have not been committed to the git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git will ignore files that have been modified but not committed.
---

**Contents**

[TOC]

#1 Using Git Ignore

Git allows users to create a file named ".gitignore" in the root of their repository. This file contains patterns and paths that Git should ignore. Any files or directories that match the patterns and paths specified in the .gitignore file will be ignored by Git and not tracked.

#2 Ignoring Unstaged Files

Git does not track unstaged files by default. To prevent Git from tracking a modified file, the user must remove the file from the staging area using the "git rm --cached" command. This command will remove the file from the staging area, but leave it in the working directory.

#3 Ignoring Committed Files

Git does not allow users to ignore committed files. However, users can use the "git update-index --assume-unchanged" command to tell Git to ignore changes to a file. This command will tell Git to assume that the file has not changed and will not stage the changes.

#4 Ignoring Uncommitted Changes

Git does not provide a way to ignore uncommitted changes. The user must manually undo any changes they have made to the file in order to restore it to its original state.
