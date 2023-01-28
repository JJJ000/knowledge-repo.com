---
title: What is the process for deleting the files in my local git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To clear your local working directory in Git, run the command `git reset --hard HEAD`.
---

**Contents**

[TOC]

### Removing Files
1. To remove files from your local working directory, you can use the `git rm` command. This command will delete the file from your working directory and stage the deletion for commit.

### Committing Deletions
2. Once you have deleted the files, you need to commit the changes. This can be done with the `git commit` command, which will commit all staged changes to the repository.

### Removing from Repository
3. To completely remove the files from your local repository, you need to push the commit to the remote repository. This can be done with the `git push` command.

### Cleaning Working Directory
4. Finally, you can use the `git clean` command to completely remove any untracked files from your local working directory. This will ensure that your local working directory is in sync with the remote repository.
