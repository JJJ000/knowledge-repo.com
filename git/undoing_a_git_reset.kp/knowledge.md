---
title: What steps can I take to reverse the effects of git reset --hard head~1?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can undo git reset --hard HEAD~1 by using the command git reflog and then git reset <commit\_id>.
---

**Contents**

[TOC]

### Solution 1
### Step 1: Checkout the Commit
Run the following command to check out the commit you want to recover:
```
git checkout <commit-hash>
```

### Step 2: Create a New Branch
Create a new branch from the commit you just checked out:
```
git branch <branch-name>
```

### Step 3: Reset the Branch to the Commit
Reset the branch to the commit you just checked out:
```
git reset --hard <commit-hash>
```

### Solution 2
### Step 1: Checkout the Commit
Run the following command to check out the commit you want to recover:
```
git checkout <commit-hash>
```

### Step 2: Create a New Branch
Create a new branch from the commit you just checked out:
```
git branch <branch-name>
```

### Step 3: Check Out the New Branch
Check out the new branch you just created:
```
git checkout <branch-name>
```

### Step 4: Merge the New Branch Into Master
Merge the new branch into the master branch:
```
git merge <branch-name>
```
