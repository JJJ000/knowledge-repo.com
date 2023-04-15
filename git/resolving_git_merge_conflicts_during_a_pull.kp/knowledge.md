---
title: Resolve any git merge conflicts in favor of the changes made during a pull
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: When resolving merge conflicts during a pull, always choose to keep the changes from the remote branch.
---

**Contents**

[TOC]

### Step 1: Identify Conflicts

Before attempting to resolve any conflicts, it is important to first identify what conflicts exist. To do this, pull the changes from the remote repository and look for any lines of code that have been changed by both you and the other user. These lines will be marked with a conflict indicator, such as “<<<<<<<”.

### Step 2: Resolve Conflicts

Once you have identified the conflicts, it is time to resolve them. This can be done by manually editing the file and replacing the conflicting lines with the version you wish to keep. Alternatively, you can use a merge tool to help you compare the different versions and select the changes you want to keep.

### Step 3: Commit Changes

After you have resolved the conflicts, you need to commit your changes. This will save the changes you have made and allow you to push them to the remote repository.

### Step 4: Push Changes

Once you have committed your changes, you can then push them to the remote repository. This will update the remote repository with your changes and allow the other user to pull them.
