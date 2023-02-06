---
title: How can I reset a remote git repository to erase all previous commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To reset a remote Git repository, use the `git push --force` command to overwrite the remote repository with the local repository.
---

**Contents**

[TOC]

1. Remove All Commits Locally
------------------------------------

To reset a remote Git repository, you must first remove all commits locally. To do this, use the `git reset` command with the `--hard` flag. This will reset your local repository to the HEAD commit and discard any uncommitted changes.

2. Push Changes to Remote
------------------------------------

Once you have removed all commits locally, you must push the changes to the remote repository. To do this, use the `git push` command with the `--force` flag. This will force the remote repository to accept the changes and overwrite the existing commits.

3. Verify Reset
------------------------------------

Finally, you should verify that the remote repository has been reset. To do this, use the `git log` command to view the commit history. If the reset was successful, the commit history should be empty.

4. Clean Up
------------------------------------

Once you have verified that the remote repository has been reset, you should clean up any local branches that you no longer need. To do this, use the `git branch` command with the `-d` flag. This will delete any local branches that are no longer needed.
