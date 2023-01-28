---
title: What is the process for undoing an initial git commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git revert <commit-hash>` to revert an initial git commit.
---

**Contents**

[TOC]

### Finding the Commit ID

The first step in reverting an initial Git commit is to find the commit ID. To do this, use the `git log` command. This command will display the commit history with the most recent commit at the top. Each commit will have a unique ID associated with it.

### Reverting the Commit

Once the commit ID has been found, the next step is to revert the commit. This can be done using the `git revert` command. The syntax for this command is `git revert <commit-id>`. This will create a new commit that will undo the changes made in the initial commit.

### Pushing the Changes

Once the commit has been reverted, the changes need to be pushed to the remote repository. This can be done using the `git push` command. The syntax for this command is `git push <remote> <branch>`. This will push the changes to the remote repository.

### Verifying the Changes

The final step is to verify that the changes have been successfully reverted. This can be done by running the `git log` command again. This will show the commit history with the reverted commit at the top. This verifies that the initial commit has been successfully reverted.
