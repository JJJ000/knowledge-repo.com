---
title: Different methods of undoing local git modifications
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The changes can be removed by using the `git checkout` or `git reset` commands.
---

**Contents**

[TOC]

### Discard All Local Changes

The simplest way to remove local changes is to discard all changes from the working directory. To do this, use the `git reset --hard HEAD` command. This command will reset the working directory to the state of the last commit, discarding all local changes.

### Discard Specific File Changes

If you only want to discard changes to a specific file, you can use the `git checkout -- <file>` command. This command will discard all changes made to the specified file and replace it with the version from the last commit.

### Stash Changes

If you want to keep your changes but remove them from the working directory, you can use the `git stash` command. This command will store all changes in a special area called the stash, which can then be reapplied at a later time.

### Revert Commits

If you have already committed changes that you want to remove, you can use the `git revert` command. This command will create a new commit that undoes the changes made in the specified commit. Note that this will not delete the original commit, but will instead create a new commit that undoes the changes.
