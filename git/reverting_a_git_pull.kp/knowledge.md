---
title: How to revert a git repository to its previous state after a pull?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Revert the changes made by the pull by resetting the repository to the commit prior to the pull.
---

**Contents**

[TOC]

### Step 1: Reset Head
Run the following command to reset the `HEAD` to the commit before the `git pull`:
```
git reset --hard HEAD~1
```

### Step 2: Undo Merge
If you are using `git merge` to pull, you can undo the merge by running the following command:
```
git merge --abort
```

### Step 3: Revert Changes
If changes were made to the files, you can revert them by running the following command:
```
git checkout .
```

### Step 4: Push Changes
Finally, push the changes to the remote repository to bring it back to the old state:
```
git push origin master
```
