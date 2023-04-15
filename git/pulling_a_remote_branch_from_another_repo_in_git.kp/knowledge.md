---
title: How to retrieve a remote branch from someone else's repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git pull <remote\_name> <branch\_name>` to pull a remote branch from somebody else`s repo.
---

**Contents**

[TOC]

### Step 1: Add Remote

You can add a remote to your local repository by running the following command:

`git remote add <remote_name> <remote_url>`

Where `<remote_name>` is the name you want to give the remote and `<remote_url>` is the URL of the remote repository.

### Step 2: Fetch Remote

Once you have added the remote, you can fetch the remote branches by running the following command:

`git fetch <remote_name>`

Where `<remote_name>` is the name you gave the remote in step 1.

### Step 3: Checkout the Remote Branch

Once you have fetched the remote branches, you can checkout the branch you want to pull from the remote repository by running the following command:

`git checkout -b <local_branch> <remote_name>/<remote_branch>`

Where `<local_branch>` is the name of the local branch you want to create, `<remote_name>` is the name you gave the remote in step 1, and `<remote_branch>` is the name of the branch you want to pull from the remote repository.

### Step 4: Pull the Remote Branch

Once you have checked out the remote branch, you can pull the branch from the remote repository by running the following command:

`git pull <remote_name> <remote_branch>`

Where `<remote_name>` is the name you gave the remote in step 1, and `<remote_branch>` is the name of the branch you want to pull from the remote repository.
