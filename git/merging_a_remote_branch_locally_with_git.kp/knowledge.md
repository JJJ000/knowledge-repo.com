---
title: Merge a remote branch of git into your local repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To merge a remote branch locally, use the command `git fetch` followed by `git merge <branch-name>`.
---

**Contents**

[TOC]

### 1. Fetch the Remote Branch

To merge a remote branch, first you need to fetch the branch from the remote repository. This can be done by using the `git fetch` command.

```git
git fetch <remote> <branch>
```

Where `<remote>` is the remote repository you want to fetch from, and `<branch>` is the branch you want to fetch. 

### 2. Checkout the Remote Branch

Once you have fetched the remote branch, you need to checkout the branch so that it is the active branch on your local repository.

```git
git checkout <branch>
```

### 3. Merge the Remote Branch

Once the remote branch is checked out, you can now merge it with your local branch.

```git
git merge <remote>/<branch>
```

Where `<remote>` is the remote repository you fetched from, and `<branch>` is the branch you want to merge.

### 4. Push the Changes

Finally, you need to push the changes to the remote repository.

```git
git push <remote> <branch>
```

Where `<remote>` is the remote repository you want to push to, and `<branch>` is the branch you want to push.
