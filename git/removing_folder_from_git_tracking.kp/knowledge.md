---
title: Stop tracking a folder in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use `git rm --cached <folder\_name>` to remove a folder from git tracking.
---

**Contents**

[TOC]

### Using the Command Line
1. Navigate to the root directory of the repository.
2. Run the following command to remove the folder from the repository: `git rm -r --cached <folder-name>`
3. Commit the changes: `git commit -m "Remove folder from repository"`
4. Push the changes to the remote repository: `git push origin <branch-name>`

### Using the GitHub Desktop App
1. Navigate to the root directory of the repository.
2. Select the folder you want to remove from the list of files and folders.
3. Right-click on the folder and select "Remove".
4. Click "Commit to master" to commit the changes.
5. Click "Push origin" to push the changes to the remote repository.
