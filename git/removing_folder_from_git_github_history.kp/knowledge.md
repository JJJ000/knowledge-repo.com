---
title: Delete folder and its contents from git/github's repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Remove a folder and its contents from git/GitHub`s history by using the `git filter-branch` command.
---

**Contents**

[TOC]

### Remove folder from local repository

1. Navigate to the folder you want to remove in your local repository.
2. Run the command `git rm -r <folder_name>` to remove the folder and its contents from the local repository.
3. Run the command `git commit -m "Remove <folder_name> and its contents"` to commit the changes.

### Remove folder from remote repository

1. Push the changes to the remote repository using the command `git push origin <branch_name>`.
2. Navigate to the remote repository in your web browser.
3. Select the branch you want to remove the folder from and click the "Commits" tab.
4. Click on the commit that removed the folder and its contents.
5. Click on the "Actions" drop-down menu and select "Revert this commit".
6. Confirm the revert by clicking "Revert commit".

### Remove folder from git/GitHub's history

1. Navigate to the remote repository in your web browser.
2. Select the branch you want to remove the folder from and click the "Commits" tab.
3. Click on the commit that removed the folder and its contents.
4. Click on the "Actions" drop-down menu and select "Remove commit from history".
5. Confirm the removal by clicking "Remove commit".

### Clean up local repository

1. Run the command `git fetch --all --prune` to clean up the local repository and remove any references to the deleted folder.
