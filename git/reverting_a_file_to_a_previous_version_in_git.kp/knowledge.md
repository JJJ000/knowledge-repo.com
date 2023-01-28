---
title: What is the process for reverting a single file to a previous version?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git checkout` command with the commit hash of the desired version.
---

**Contents**

[TOC]

### Step 1: Checkout the Previous Version

Use the `git checkout` command to checkout the previous version of the file you want to revert. 

```
git checkout <commit-hash> <file-name>
```

### Step 2: Check the Status

Check the status of the file to make sure it has been reverted correctly.

```
git status
```

### Step 3: Commit the Revert

Use the `git commit` command to commit the revert.

```
git commit -m "Revert to previous version"
```

### Step 4: Push the Commit

Push the commit to the remote repository.

```
git push origin <branch-name>
```
