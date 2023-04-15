---
title: How to delete a remote origin from a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run the command `git remote remove origin` to remove the remote origin from a Git repository.
---

**Contents**

[TOC]

### Removing Remote Origin
To remove a remote origin from a Git repository, use the command:

`git remote rm <name>`

Where `<name>` is the name of the remote origin you want to remove.

### Confirming the Removal
To confirm that the remote origin has been removed, use the command:

`git remote -v`

This will list all the remote origins associated with the repository. If the remote origin you removed is no longer listed, then it has been successfully removed.

### Removing Remote Branches
It is important to note that removing a remote origin does not automatically remove any associated remote branches. To remove a remote branch, use the command:

`git push <name> --delete <branch>`

Where `<name>` is the name of the remote origin you want to remove the branch from, and `<branch>` is the name of the branch you want to remove.

### Confirming the Removal
To confirm that the remote branch has been removed, use the command:

`git branch -r`

This will list all the remote branches associated with the repository. If the remote branch you removed is no longer listed, then it has been successfully removed.
