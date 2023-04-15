---
title: Sync a submodule to the most recent commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git submodule update --remote --merge` to update a submodule to the latest commit in Git.
---

**Contents**

[TOC]

### Step 1: Navigate to the Submodule Directory

Change your working directory to the submodule directory.

```
cd <path/to/submodule>
```

### Step 2: Fetch Latest Changes

Fetch the latest changes from the remote repository.

```
git fetch
```

### Step 3: Checkout the Latest Commit

Checkout the latest commit from the remote repository.

```
git checkout <commit-id>
```

### Step 4: Update the Submodule

Update the submodule to the latest commit.

```
git submodule update --remote --merge
```
