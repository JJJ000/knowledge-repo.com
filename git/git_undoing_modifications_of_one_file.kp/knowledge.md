---
title: Revert changes to a single file in git's working copy
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To undo the working copy modifications of one file in Git, use the `git checkout` command.
---

**Contents**

[TOC]

### Discard All Local Changes

You can discard all local changes in one file with the following command:

`git checkout -- <file_name>`

This will reset the file to the last commit and discard all local changes.

### Discard Selected Local Changes

If you want to discard select local changes, you can use the `git checkout` command with the `--patch` option. This will open an interactive prompt where you can select which changes to discard.

The command is as follows:

`git checkout --patch <file_name>`

### Undo Last Commit

If you want to undo the last commit, you can use the `git reset` command with the `--soft` option. This will reset the file to the previous commit and keep the local changes.

The command is as follows:

`git reset --soft HEAD~1 <file_name>`

### Revert to a Specific Commit

If you want to revert to a specific commit, you can use the `git reset` command with the `--hard` option. This will reset the file to the specified commit and discard all local changes.

The command is as follows:

`git reset --hard <commit_hash> <file_name>`
