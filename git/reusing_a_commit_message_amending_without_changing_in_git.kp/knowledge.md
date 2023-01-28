---
title: How can I amend a commit without altering the original commit message?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git commit --amend --no-edit` to amend a commit without changing the commit message.
---

**Contents**

[TOC]

### Step 1: Amend the Commit
1. Checkout the commit you want to amend:
   ```git
   git checkout <commit-hash>
   ```
2. Make the necessary changes to the repository.
3. Commit the changes with the `--amend` flag:
   ```git
   git commit --amend
   ```

### Step 2: Force Push the Change
1. Force push the amended commit:
   ```git
   git push --force <remote-name> <branch-name>
   ```
2. If you're pushing to a remote repository, you may need to add the `--force-with-lease` flag to ensure you don't overwrite any other changes:
   ```git
   git push --force-with-lease <remote-name> <branch-name>
   ```

### Step 3: Confirm the Change
1. Confirm that the amended commit is pushed to the remote repository.
2. Check the commit message to confirm it is the same as the previous commit.
