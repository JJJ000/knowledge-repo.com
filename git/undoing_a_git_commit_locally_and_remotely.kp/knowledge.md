---
title: How can I undo a "git commit" both locally and on a remote after it has been pushed?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can undo a `git commit` locally and on a remote after `git push` by using the `git revert` command.
---

**Contents**

[TOC]

### Undo a Git Commit Locally
1. Check the commit log to find the commit you want to undo: `git log`
2. Copy the commit hash of the commit you want to undo
3. Revert the commit: `git revert <commit-hash>`

### Undo a Git Commit on a Remote
1. Check the commit log to find the commit you want to undo: `git log`
2. Copy the commit hash of the commit you want to undo
3. Push the revert commit to the remote: `git push origin <commit-hash>`
