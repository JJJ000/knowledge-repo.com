---
title: What steps do I need to take to resolve a merge conflict caused by the deletion of a file in a branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Resolve the conflict by either restoring the file in the branch or removing the file from the other branch.
---

**Contents**

[TOC]

### Step 1: Identify the Conflict

The first step to resolving a merge conflict due to removal of a file in a branch in Git is to identify the conflict. This can be done by running `git status` which will show any conflicts that have occurred during the merge. 

### Step 2: Resolve the Conflict

Once the conflict has been identified, the next step is to resolve it. This can be done by examining the changes made to the file in each branch and deciding which changes should be kept. If the file was removed in one branch, then it should be removed in the merged branch. 

### Step 3: Commit the Resolution

Once the conflict has been resolved, the changes need to be committed. This can be done by running `git add <file>` and then `git commit -m "Resolved merge conflict"`. This will commit the changes and mark the conflict as resolved.

### Step 4: Push the Changes

Finally, the changes need to be pushed to the remote repository. This can be done by running `git push origin <branch>`. This will push the changes to the remote repository and the merge conflict will be resolved.
