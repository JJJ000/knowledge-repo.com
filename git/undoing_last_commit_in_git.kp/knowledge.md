---
title: What is the procedure for reverting the last commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To undo the last commit in Git, use the `git reset --hard HEAD~1` command.
---

**Contents**

[TOC]

#### Step 1: Checkout the Previous Commit
Run the following command to checkout the previous commit:

```git checkout HEAD~1```

#### Step 2: Reset the Commit
Run the following command to reset the commit:

```git reset --hard HEAD~1```

#### Step 3: Push the Changes
Run the following command to push the changes:

```git push origin <branch_name> --force```

#### Step 4: Clean Up
Run the following command to clean up the local repository:

```git clean -f```
