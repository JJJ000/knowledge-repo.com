---
title: Revert git update-index --assume-unchanged <file>
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To undo the git update-index --assume-unchanged <file> command, run git update-index --no-assume-unchanged <file>.
---

**Contents**

[TOC]

### Revert to Tracking

To undo the `git update-index --assume-unchanged <file>` command, you can use the `git update-index --no-assume-unchanged <file>` command. This will revert the file back to being tracked by git.

### Unstage Changes

If the file has been modified since it was set to `--assume-unchanged`, the changes will not be reflected in the git repository. To unstage these changes, you can use the `git reset <file>` command. This will unstage the changes and allow you to commit them to the repository.

### Revert to Previous Commit

If the changes made to the file since it was set to `--assume-unchanged` have already been committed, you can use the `git revert <file>` command to revert the file back to its previous commit. This will discard any changes made since the last commit and restore the file to its previous state.

### Discard Unstaged Changes

If you want to discard any changes made to the file since it was set to `--assume-unchanged`, you can use the `git checkout <file>` command. This will discard any unstaged changes and reset the file back to the last committed version.
