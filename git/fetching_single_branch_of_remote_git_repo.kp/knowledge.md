---
title: What is the procedure for retrieving a single branch from a remote git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git fetch <remote\_name> <branch\_name>` to fetch only one branch of a remote Git repository.
---

**Contents**

[TOC]

### 1. Clone the Remote Repository
In order to fetch only one branch of a remote Git repository, the repository must first be cloned. To clone a remote repository, use the `git clone` command. For example, to clone the remote repository `git@github.com:username/repo.git` to the local directory `/path/to/local/directory`, the following command can be used:

```
git clone git@github.com:username/repo.git /path/to/local/directory
```

### 2. Checkout the Desired Branch
Once the remote repository has been cloned, the desired branch can be checked out. To checkout a branch, use the `git checkout` command. For example, to checkout the branch `my-branch` in the cloned repository, the following command can be used:

```
git checkout my-branch
```

### 3. Fetch the Desired Branch
Once the desired branch has been checked out, it can be fetched. To fetch a branch, use the `git fetch` command. For example, to fetch the branch `my-branch` in the cloned repository, the following command can be used:

```
git fetch origin my-branch
```

### 4. Pull the Desired Branch
Once the desired branch has been fetched, it can be pulled. To pull a branch, use the `git pull` command. For example, to pull the branch `my-branch` in the cloned repository, the following command can be used:

```
git pull origin my-branch
```
