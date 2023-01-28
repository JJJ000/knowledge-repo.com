---
title: Revert git branch to original version
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can reset a git branch to its origin version by using the `git reset --hard origin/branch\_name` command.
---

**Contents**

[TOC]

### Back Up Your Repository

Before making any changes to your repository, it is important to back up your repository in case you need to restore it to its current state. You can back up your repository by creating a new branch and committing your changes.

### Reset Your Branch to Origin

Once you have backed up your repository, you can reset your branch to origin. To do this, you need to run the following command:

`git reset --hard origin/<branch-name>`

This command will reset your branch to the state it was in when it was originally created.

### Push the Changes

Once you have reset your branch to origin, you need to push the changes to the remote repository. To do this, you need to run the following command:

`git push -f origin <branch-name>`

This command will push the changes to the remote repository.

### Verify the Changes

Finally, you need to verify that the changes have been successfully pushed to the remote repository. To do this, you need to run the following command:

`git log --oneline --decorate --graph --all`

This command will show you the list of commits that have been pushed to the remote repository. If the changes have been successfully pushed, you should see the reset commit in the list.
