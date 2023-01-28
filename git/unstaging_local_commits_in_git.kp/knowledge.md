---
title: What is the process for reverting back to an unstaged version of my files after I have made a local commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the `git reset HEAD <file>` command to unstage your files after making a local commit.
---

**Contents**

[TOC]

### Using `git reset`

Using `git reset` is the most common way to unstage files after making a local commit. The command `git reset` reverts the changes made in the working directory and moves the HEAD pointer back to the previous commit.

To unstage files, use the command `git reset <file>`, where `<file>` is the name of the file you want to unstage.

### Using `git checkout`

Another way to unstage files is to use the command `git checkout <file>`, where `<file>` is the name of the file you want to unstage. This command will reset the file to its state at the last commit, effectively undoing the changes made since the last commit.

### Using `git revert`

You can also use the command `git revert` to unstage files. This command will create a new commit that reverts the changes made in the working directory.

To use `git revert`, use the command `git revert <commit>`, where `<commit>` is the commit you want to revert. This will create a new commit that reverts the changes made in the working directory.
