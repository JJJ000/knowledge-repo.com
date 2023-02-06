---
title: Store modifications while preserving the modifications in the working tree in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use `git stash` to save changes to the stash while keeping them in the working directory.
---

**Contents**

[TOC]

#### Stashing the Changes

To stash changes in Git, use the `git stash` command. This command will take all of the changes in the working directory and save them in a temporary stash that can be accessed later.

#### Accessing the Stash

To access the stash, use the `git stash list` command. This command will list all of the stashes that have been saved. To access a specific stash, use the `git stash apply` command followed by the stash name.

#### Unstashing the Changes

To unstash the changes, use the `git stash pop` command. This command will apply the changes from the stash and remove the stash from the list.

#### Removing the Stash

To remove the stash from the list without applying the changes, use the `git stash drop` command followed by the stash name. This command will remove the stash from the list without applying the changes.
