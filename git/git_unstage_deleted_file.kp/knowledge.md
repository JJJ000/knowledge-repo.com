---
title: Revert a deleted file in git to an unstaged state
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git reset HEAD <file>`.
---

**Contents**

[TOC]

### Restoring a Deleted File

### Check the Git Repository
Git stores a repository of all the changes made to the project. To restore a deleted file, first check the repository to make sure the file is still there. To do this, use the `git log --diff-filter=D --summary` command to view a list of all deleted files.

### Check the Stash
If the file was deleted recently, it may still be in the stash. To check the stash, use the `git stash list` command. If the deleted file is in the stash, use `git stash apply` to restore it.

### Check Previous Commits
If the file is not in the repository or the stash, it may still be in a previous commit. To check previous commits, use the `git log` command and look for the deleted file. If the file is found, use `git checkout <commit_id> <file_name>` to restore the file.

### Restore from Backup
If the file is not in the repository, stash, or previous commits, it may still be possible to restore it from a backup. If a backup exists, use the appropriate tool to restore the file from the backup.
