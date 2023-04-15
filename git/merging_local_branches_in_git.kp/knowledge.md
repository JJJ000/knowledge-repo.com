---
title: Combine one local branch into another local branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To merge one local branch into another local branch in Git, use the command `git merge <branch\_name>`.
---

**Contents**

[TOC]

### Step 1: Fetch from Remote

First, you need to fetch the most recent version of the remote branch to your local repository. This can be done by using the following command:

`git fetch origin <remote_branch_name>`

### Step 2: Checkout Local Branch

Next, you need to checkout the local branch you want to merge into:

`git checkout <local_branch_name>`

### Step 3: Merge Remote Branch

Once you have the local branch checked out, you can merge the remote branch into it using the following command:

`git merge origin/<remote_branch_name>`

### Step 4: Push to Remote

Finally, you need to push the changes to the remote repository. This can be done with the following command:

`git push origin <local_branch_name>`
