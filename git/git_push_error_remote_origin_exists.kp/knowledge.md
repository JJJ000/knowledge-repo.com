---
title: 'an existing remote origin is already present when pushing to a new repository using 'git push'
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No, a new remote origin must be added before pushing to a new repository.
---

**Contents**

[TOC]

### Existing Remote Origin
When a local repository is pushed to a remote repository for the first time, the remote repository is automatically set as the origin for the local repository. This means that when the `git push` command is used, the changes from the local repository are pushed to the remote repository.

### Updating Remote Origin
If the local repository is pushed to a different remote repository, the origin of the local repository must be updated. This can be done using the `git remote set-url` command. The `set-url` command allows the user to update the remote origin of the local repository, so that the `git push` command will push the changes to the new remote repository.

### Deleting Remote Origin
If the user wishes to delete the existing remote origin, they can use the `git remote rm` command. This will delete the existing remote origin from the local repository, and the `git push` command will no longer push changes to the remote repository.

### Adding New Remote Origin
Once the existing remote origin has been deleted, the user can add a new remote origin to the local repository with the `git remote add` command. This command allows the user to add a new remote repository, and the `git push` command will then push changes to the new remote repository.
