---
title: What is the process for reverting my most recent commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To uncommit the last commit in Git, use the command `git reset --soft HEAD~1`.
---

**Contents**

[TOC]

### Check the Commit History

To start, you'll need to check the commit history to identify the commit you want to undo. You can do this by running the following command in the terminal:

`$ git log`

This will print out a list of all the commits in the repository, with the most recent at the top.

### Reset Your Head

Once you have identified the commit you want to undo, you can undo it by running the following command:

`$ git reset HEAD~1`

This will move your HEAD pointer back one commit, effectively undoing the most recent commit.

### Push the Changes

Now that you have undone the commit, you need to push the changes to the remote repository. You can do this by running the following command:

`$ git push -f`

This will force push the changes to the remote repository, effectively undoing the most recent commit.

### Clean Up

Finally, you need to clean up any local changes that were created by the undo. You can do this by running the following command:

`$ git clean -f`

This will delete any untracked files or directories that were created by the undo.
