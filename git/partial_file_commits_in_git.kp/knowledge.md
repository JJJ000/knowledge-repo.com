---
title: In git, is it possible to make only certain modifications to a file and save them?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Yes, you can commit only part of a file`s changes in Git by staging the changes before committing.
---

**Contents**

[TOC]

### Using Git Stash

Git Stash is a great way to save changes to a file without committing them. To use Git Stash, first make the changes to the file you want to commit, then run the command `git stash`. This will save the changes to a stash and remove them from the working directory. When you're ready to commit the changes, run the command `git stash pop` to restore the changes to the working directory.

### Using Git Add

Another way to commit only part of a file's changes is to use the `git add` command. First, make the changes to the file you want to commit. Then, use the `git add -p` command to bring up an interactive prompt. This will allow you to choose which sections of the file you want to commit. When you're finished, use the `git commit` command to commit the changes.

### Using Git Patch

The `git patch` command is another way to commit only part of a file's changes. To use this command, make the changes to the file you want to commit. Then, run the command `git diff > patch.diff` to create a patch file containing the changes. Finally, use the `git apply patch.diff` command to apply the patch to the working directory. This will commit only the changes specified in the patch file.
