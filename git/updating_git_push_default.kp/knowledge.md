---
title: Altering the default 'push to' setting for the git remote
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The default remote `push to` can be changed by running the command `git remote set-url <remote> <url>`.
---

**Contents**

[TOC]

`` Changing the Remote Push URL

1. Open the command line and navigate to the local repository.
2. Type `git remote -v` to view the current remote repository URL.
3. Type `git remote set-url <new-url>` to change the remote repository URL.
4. Type `git remote -v` again to verify the new URL.

`` Setting the Default Push Remote

1. Type `git config --global push.default simple` to set the default push remote.
2. Type `git config --list` to verify the default push remote has been set.

`` Setting the Push Branch

1. Type `git config --global push.default current` to set the default push branch.
2. Type `git config --list` to verify the default push branch has been set.

`` Verifying the Changes

1. Type `git push` to push the changes to the remote repository.
2. Type `git remote -v` to verify the remote repository URL is correct.
