---
title: Pull changes from the master branch into your branch in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To get changes from the master branch into a branch, use the git pull command.
---

**Contents**

[TOC]

### Step 1: Checkout Your Branch

Before you can start integrating changes from the master branch, you need to make sure you are on the branch you want to merge changes into. To do this, use the `git checkout` command to switch to the branch:

```
git checkout <branch-name>
```

### Step 2: Fetch Latest Changes

Once you are on the correct branch, you need to fetch the latest changes from the master branch. This will ensure you have the most up-to-date version of the master branch. To do this, use the `git fetch` command:

```
git fetch origin master
```

### Step 3: Merge Changes

Now that you have the latest changes from the master branch, you can merge them into your branch. To do this, use the `git merge` command:

```
git merge origin/master
```

### Step 4: Push Changes

Finally, you need to push the changes to your branch. To do this, use the `git push` command:

```
git push origin <branch-name>
```
