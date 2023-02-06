---
title: Push the most recent commit to the remote repository using git's 'reset --hard' command
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can reset the local repository to the remote repository`s state with `git reset --hard` and then push the changes with `git push -f`.
---

**Contents**

[TOC]

### Pros

* This command can be used to discard all local changes, which can be useful when you mess up your local repository and need to start over.

* It can also be used to quickly switch between different versions of your repository.

### Cons

* Resetting to a previous commit can cause you to lose any changes that have been made since that commit.

* Pushing to the remote repository after a reset can overwrite any changes that have been made by other users. This can cause confusion and lead to data loss.

### Alternatives

* If you need to discard local changes, you can use the `git stash` command to save them for later.

* If you need to switch between different versions of your repository, you can use the `git checkout` command.

* If you need to push changes to the remote repository, you should use the `git push` command.
