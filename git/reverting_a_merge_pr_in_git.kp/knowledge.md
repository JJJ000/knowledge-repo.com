---
title: Revert a merge by pull request?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can undo a merge by reverting the merge commit that was created when the pull request was merged.
---

**Contents**

[TOC]

# Revert the Merge Commit
1. Checkout the branch you want to revert the merge to.
   ```git checkout <branch-name>```
2. Revert the merge commit.
   ```git revert -m 1 <merge-commit-sha>```

# Push Reverted Changes
1. Push the reverted changes.
   ```git push origin <branch-name>```
2. Check the status of the branch on the remote repository.
   ```git status```
