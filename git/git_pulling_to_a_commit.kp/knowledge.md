---
title: Retrieve changes from a remote repository up to a specified commit using git pull
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can git pull to a particular commit by using the commit`s SHA-1 hash.
---

**Contents**

[TOC]

# Git Pull to a Particular Commit

## Step 1: Checkout the Commit

To pull a particular commit, the first step is to checkout the commit. This can be done by using the `git checkout` command and specifying the commit's hash.

```
git checkout <commit-hash>
```

## Step 2: Pull the Commit

Once the commit has been checked out, the next step is to pull the commit. This can be done by using the `git pull` command.

```
git pull
```

## Step 3: Push the Commit

Finally, the commit needs to be pushed to the remote repository. This can be done by using the `git push` command.

```
git push
```
