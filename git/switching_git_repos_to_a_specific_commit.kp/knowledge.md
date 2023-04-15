---
title: What is the best way to revert my git repository to a specific commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can switch your git repository to a particular commit by using the command `git reset --hard <commit-hash>`.
---

**Contents**

[TOC]

1. **Checkout the Commit**

- Use the `git checkout` command followed by the commit hash.

   `git checkout <commit-hash>`

2. **Create a New Branch**

- Create a new branch from the commit you just checked out.

   `git checkout -b <branch-name>`

3. **Switch to the New Branch**

- Switch to the new branch you just created.

   `git checkout <branch-name>`

4. **Push the New Branch to Remote**

- Push the new branch to remote.

   `git push -u origin <branch-name>`
