---
title: What is the best way to combine my last n commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: You can use `git rebase -i HEAD~N` to squash your last N commits together.
---

**Contents**

[TOC]

### Step 1: Find the SHA-1 of the Commit You Want to Squash

The first step in squashing your last N commits together is to find the SHA-1 of the commit you want to squash. To do this, run the command `git log` to view the commit history. This will display a list of all your commits, with the most recent at the top. Look for the commit you want to squash and copy its SHA-1.

### Step 2: Checkout the Commit You Want to Squash

Once you have the SHA-1 of the commit you want to squash, you need to checkout that commit. To do this, run the command `git checkout <sha-1 of the commit>`. This will checkout the commit you want to squash.

### Step 3: Squash the Commits

Now that you have checked out the commit you want to squash, you can run the command `git rebase -i HEAD~N`, where N is the number of commits you want to squash together. This will open up your default text editor with a list of all your commits. Replace all the words “pick” with “squash”, except for the first one. This will squash all the commits together.

### Step 4: Push the Changes

Finally, once you have squashed the commits together, you need to push the changes to the remote repository. To do this, run the command `git push -f origin <branch name>`. This will push the changes to the remote repository and squash your commits together.
