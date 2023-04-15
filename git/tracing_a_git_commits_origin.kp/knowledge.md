---
title: Determining which branch a git commit originated from
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can find out what branch a Git commit came from by checking the commit`s log or by using the command `git branch --contains <commit-hash>`.
---

**Contents**

[TOC]

### Finding the Branch

1. Start by finding the commit hash for the commit you are looking for.
2. Run the command `git branch --contains <commit-hash>`. This will list all branches containing the commit.
3. Select the branch you are looking for from the list.

### Viewing the Commit

1. Run the command `git checkout <branch-name>`. This will switch you to the branch containing the commit you are looking for.
2. Run the command `git log`. This will list the commits in the branch.
3. Find the commit you are looking for and review the commit message and changes.
