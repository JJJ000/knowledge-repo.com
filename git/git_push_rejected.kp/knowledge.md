---
title: The remote rejected the git push because the master branch is currently checked out
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The push cannot be completed because the branch is currently checked out on the remote.
---

**Contents**

[TOC]

### Solution

### Overview

Git push error '[remote rejected] master -> master (branch is currently checked out)' occurs when a user attempts to push changes to a remote repository, but the remote repository has a branch that is currently checked out. The error occurs because the remote repository cannot accept changes to a branch that is currently checked out.

### Causes

This error occurs when a user attempts to push changes to a remote repository, but the remote repository has a branch that is currently checked out. 

The remote repository cannot accept changes to a branch that is currently checked out, so the push is rejected.

### Solutions

To resolve this error, the user must either switch to a different branch on the remote repository, or commit their changes to the branch that is currently checked out.

Once the branch is no longer checked out on the remote repository, the user can then push their changes.
