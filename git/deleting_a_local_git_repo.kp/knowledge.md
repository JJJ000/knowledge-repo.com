---
title: What is the process for removing a local git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To delete a local repository in git, run the command `git rm -r <repository name>`.
---

**Contents**

[TOC]

### Deleting the Repository
1. Open your terminal and navigate to the local repository you want to delete.
2. Run the command `git rm -rf .` to delete all files in the repository.
3. Run `rm -rf .git` to delete the repository's Git data.

### Removing the Repository from the Remote Server
1. Log into the remote server.
2. Navigate to the repository folder.
3. Run the command `rm -rf <repository name>` to delete the repository.
