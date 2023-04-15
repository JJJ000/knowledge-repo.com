---
title: What is the process for returning a file to a particular version?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To reset or revert a file to a specific revision in Git, use the `git reset` command with the `--hard` flag and the desired commit hash.
---

**Contents**

[TOC]

### Using Git Reset
1. Check the commit history to identify the revision you want to revert to.
2. Run the command `git reset --hard <commit_id>` to reset the file to the specified revision.
3. To update the remote repository with the new revision, run `git push --force <remote_name> <branch_name>`.

### Using Git Revert
1. Check the commit history to identify the revision you want to revert to.
2. Run the command `git revert <commit_id>` to create a new commit reverting the specified revision.
3. Push the new commit to the remote repository with `git push <remote_name> <branch_name>`.
