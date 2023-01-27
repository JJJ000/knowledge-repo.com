---
title: Is it possible to remove a git commit while preserving the modifications?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Yes, you can use the `git reset` command with the `--soft` option to delete a commit while keeping the changes.
---

**Contents**

[TOC]

### Revert the Commit
One way to delete a git commit but keep the changes is to revert the commit. To do this, you can use the `git revert` command. This will create a new commit that undoes all the changes made in the original commit.

### Reset the Commit
Another way to delete a git commit but keep the changes is to reset the commit. To do this, you can use the `git reset` command. This will move the HEAD pointer back to the commit before the one you want to delete, and all changes made in the commit will remain in the working directory.

### Discard the Commit
A third way to delete a git commit but keep the changes is to discard the commit. To do this, you can use the `git checkout` command. This will discard all changes made in the commit and leave the working directory as it was before the commit was made.
