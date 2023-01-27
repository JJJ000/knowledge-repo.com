---
title: What is the process for retrieving a lost commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the `git stash apply` command to recover a dropped stash in Git.
---

**Contents**

[TOC]

#1 Finding the Stash

Git stores information about stashes in its reflog. You can use the following command to search the reflog for references to a dropped stash:

`git reflog | grep "stash@"`

This command will output a list of all stashes that are stored in the reflog.

#2 Recovering the Stash

Once you have identified the stash that you want to recover, you can use the following command to recover it:

`git stash apply <stash-name>`

Where <stash-name> is the name of the stash that you want to recover.

#3 Cleaning Up

Once you have recovered the stash, you may want to remove it from the reflog. You can do this with the following command:

`git stash drop <stash-name>`

Where <stash-name> is the name of the stash that you want to delete.

#4 Verifying the Recovery

Once you have recovered the stash and deleted it from the reflog, you can verify that the recovery was successful by running the following command:

`git stash list`

This command will output a list of all stashes that are currently stored in the repository. If the stash that you recovered is not listed, then the recovery was successful.
