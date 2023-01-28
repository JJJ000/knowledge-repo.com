---
title: How can I push my current changes to a different branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Checkout the desired branch, then use `git commit` to commit your changes.
---

**Contents**

[TOC]

### 1. Checkout the Target Branch

To commit your changes to a different branch, first you need to checkout the target branch.

`git checkout <target-branch>`

### 2. Commit Your Changes

Once you have checked out the target branch, you can commit your changes.

`git commit -m "Commit message"`

### 3. Push Your Changes

Finally, you need to push your changes to the remote repository.

`git push origin <target-branch>`

### 4. Verify the Changes

To verify that your changes have been committed to the target branch, you can list the branches in your repository.

`git branch -a`
