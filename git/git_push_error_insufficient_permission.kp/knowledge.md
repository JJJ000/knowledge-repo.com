---
title: Error insufficient permission when attempting to add an object to the git repository database
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You need to have write permissions on the repository to be able to push changes.
---

**Contents**

[TOC]

### Solution

### Check Permissions

The first step to solving this error is to check the permissions associated with the repository. This can be done by navigating to the repository's settings page and checking the permissions associated with it. If the user does not have sufficient permissions to push to the repository, they will need to contact the repository's owner and request access.

### Check SSH Keys

The next step is to check that the correct SSH keys are being used for the push. If the user is using an SSH key that is not associated with the repository, then the push will fail. To check which SSH key is being used, the user can run the command `ssh-add -l` in the terminal. If the correct SSH key is not listed, the user can add it by running the command `ssh-add <path/to/ssh/key>`.

### Check Branch

The user should also check that they are pushing to the correct branch. If the user is pushing to a branch that does not exist, or a branch that they do not have permission to push to, then the push will fail. To check which branch the user is pushing to, they can run the command `git branch -a` in the terminal.

### Check Remote

Finally, the user should check that the correct remote is being used for the push. If the user is pushing to a remote that does not exist, or a remote that they do not have permission to push to, then the push will fail. To check which remote the user is pushing to, they can run the command `git remote -v` in the terminal.
