---
title: What is the process for reverting a "git commit --amend" instead of a "git commit"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can undo the amend commit by running `git reset --soft HEAD~1` to reset the HEAD pointer to the previous commit.
---

**Contents**

[TOC]

### Step 1: Revert the commit

You can use the following command to revert the commit:

`git revert <commit-hash>`

The commit-hash is the unique identifier for the commit you want to revert.

### Step 2: Push the revert commit

After reverting the commit, you need to push the revert commit to your remote repository:

`git push origin <branch-name>`

### Step 3: Undo the amend

You can also undo the amend by using the following command:

`git reset --soft HEAD^`

This command will undo the amend and will leave the changes in the staging area.

### Step 4: Commit the changes

Finally, you need to commit the changes again:

`git commit -m "Commit message"`

This will create a new commit with the changes you have made.
