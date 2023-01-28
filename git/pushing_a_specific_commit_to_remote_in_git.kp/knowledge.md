---
title: What is the best way to send a particular commit to a remote repository without including any prior commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the `git push <remote> <commit-SHA>` command to push a specific commit to a remote without pushing previous commits.
---

**Contents**

[TOC]

### 1. Checkout the Specific Commit

Using `git checkout` you can checkout the specific commit you want to push.

```
git checkout <commit-hash>
```

### 2. Create a New Branch

Create a new branch from the specific commit to push it to the remote.

```
git checkout -b <branch-name>
```

### 3. Push the New Branch

Push the new branch to the remote.

```
git push origin <branch-name>
```

### 4. Cleanup

Once the new branch is pushed, you can delete the branch and checkout your original branch.

```
git branch -d <branch-name>
git checkout <original-branch>
```
