---
title: What is the best way to delete files that are included in the .gitignore but still present on the repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git rm -r --cached .` to remove all files listed in the .gitignore from the repository.
---

**Contents**

[TOC]

### Step 1: Find the Files 

To remove files listed in the .gitignore but still on the repository, you must first identify them. To do this, you can use the `git ls-files` command. This command will list all the files that are currently being tracked by Git. 

### Step 2: Remove the Files

Once you have identified the files that need to be removed, you can use the `git rm` command to remove them from the repository. This command will delete the file from the repository and also remove it from the staging area.

### Step 3: Commit the Changes

Once you have removed the files, you must commit the changes. This will ensure that the files are permanently removed from the repository. To commit the changes, use the `git commit` command with the `-m` flag to add a commit message.

### Step 4: Push the Changes

Finally, you must push the changes to the remote repository. This will ensure that the changes are reflected on the remote repository. To do this, use the `git push` command.
