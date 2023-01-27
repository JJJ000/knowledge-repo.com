---
title: What is the process for reverting to a previous commit using 'git reset --hard head'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To revert to a previous commit using `git reset --hard HEAD`, use the commit hash of the commit you want to revert to.
---

**Contents**

[TOC]

### Step 1: Identify the Previous Commit

To revert to a previous commit, you first need to identify the commit you want to revert to. This can be done by running the command `git log` which will list all of the commits in the repository. Each commit will have a unique identifier associated with it that can be used to reference the commit.

### Step 2: Run the Reset Command

Once you have identified the commit you want to revert to, you can use the `git reset --hard HEAD` command. This command will reset the repository back to the commit specified. 

### Step 3: Push the Commit 

Finally, once the reset is complete, you can push the commit back to the remote repository using the `git push` command. This will ensure that the remote repository is in sync with the local repository.

### Step 4: Clean Up

Once the commit has been pushed, you can clean up any local changes that were made after the commit by running the `git clean -f` command. This will remove any untracked files and directories that were created after the commit.
