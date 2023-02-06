---
title: How to stop pushing with git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To disable pushing to a repository, use the command `git push --mirror --dry-run`.
---

**Contents**

[TOC]

# Disabling Push to a Remote Repository

1. Identify the Remote Repository 
   To disable push to a remote repository, first identify the remote repository you want to disable push to.

2. Use `git remote` 
   To disable push to a remote repository, use the `git remote` command. This command allows you to view and manage the remote repositories associated with your local repository.

3. Use `--mirror` 
   To disable push to a remote repository, use the `--mirror` option with the `git remote` command. This option will disable push to the specified remote repository.

4. Push Changes 
   Once you have disabled push to the remote repository, you can then push your changes to the local repository.
