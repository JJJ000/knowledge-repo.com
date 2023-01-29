---
title: What is the process for reverting a stash?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To reverse apply a stash in Git, use the `git stash apply --index --reverse` command.
---

**Contents**

[TOC]

#1 Reverting the Stash
To reverse apply a stash in Git, the user must first revert the stash. This can be done by using the command `git stash apply --index --reverse` on the terminal. This command will restore the state of the working directory to the state it was in before the stash was applied.

#2 Removing the Stash
Once the stash has been reverted, the user must then remove it from the list of stashes. This can be done by using the command `git stash drop` on the terminal. This command will delete the stash from the list of stashes and free up space in the repository.

#3 Verifying the Changes
The user should then verify that the changes made by reverting the stash have been properly applied. This can be done by using the command `git diff` on the terminal. This command will show the differences between the current working directory and the state it was in before the stash was applied.

#4 Committing the Changes
Once the user has verified the changes, they should commit them to the repository. This can be done by using the command `git commit` on the terminal. This command will add the changes to the repository and make them a permanent part of the project's history.
