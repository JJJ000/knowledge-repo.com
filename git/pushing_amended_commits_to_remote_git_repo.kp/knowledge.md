---
title: How can I upload my revised commit to the remote git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git push origin <your\_branch\_name>` to push the amended commit to the remote Git repository.
---

**Contents**

[TOC]

### Step 1: Amend the Commit

The first step is to amend the commit that you want to push to the remote Git repository. To do so, use the `git commit --amend` command. This command allows you to modify the commit message, add additional files to the commit, or even change the content of the files that were already included in the commit. 

### Step 2: Force Push the Commit

Once the commit has been amended, you must use the `git push --force` command to push the amended commit to the remote Git repository. This command will overwrite the existing commit on the remote repository with the amended commit. 

### Step 3: Confirm Push

The third step is to confirm that the amended commit has been successfully pushed to the remote repository. To do so, use the `git log` command to view the commit history of the remote repository. If the amended commit is present, then the push was successful. 

### Step 4: Clean Up

Finally, it is important to clean up any local branches that were created during the process of amending the commit. To do so, use the `git branch -D <branch_name>` command to delete any local branches that were created. This will ensure that the local repository does not contain any unnecessary branches.
