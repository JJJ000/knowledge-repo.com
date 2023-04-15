---
title: How to pull changes from the master branch into the development branch using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To pull from master into the development branch, run `git pull origin masterdevelopment`.
---

**Contents**

[TOC]

### Step 1: Checkout the Development Branch

In order to pull from the master branch into the development branch, you must first checkout the development branch. To do this, use the following command:

```
git checkout development
```

### Step 2: Pull from Master

Once you have checked out the development branch, you can pull from the master branch. To do this, use the following command:

```
git pull origin master
```

### Step 3: Resolve Merge Conflicts

If there are any merge conflicts, you will need to resolve them before the pull can be completed. To do this, you will need to edit the files with the merge conflicts and resolve the conflicts manually.

### Step 4: Push to Development

Once all merge conflicts have been resolved, you can push the changes to the development branch. To do this, use the following command:

```
git push origin development
```
