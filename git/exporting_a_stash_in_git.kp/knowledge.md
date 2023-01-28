---
title: Transfer a stash to another computer
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git stash apply` on the other computer to import the stash.
---

**Contents**

[TOC]

#1 Cloning the Stash

The first step in exporting a stash to another computer in Git is to clone the stash. This can be done by using the `git clone` command, followed by the URL of the stash. This will create a local copy of the stash on the computer.

#2 Pulling the Stash

Once the stash is cloned, the next step is to pull the stash from the remote repository. This can be done by using the `git pull` command, followed by the URL of the remote stash. This will pull any changes from the remote repository that have not yet been pulled into the local copy of the stash.

#3 Pushing the Stash

Once the stash has been pulled from the remote repository, the next step is to push the stash to the other computer. This can be done by using the `git push` command, followed by the URL of the other computer. This will push any changes from the local copy of the stash to the other computer.

#4 Confirming the Push

Once the push is complete, the last step is to confirm that the push was successful. This can be done by using the `git status` command. This will show any changes that have been pushed to the other computer. If the changes have been successfully pushed, the output of the command should show that the stash is up to date.
