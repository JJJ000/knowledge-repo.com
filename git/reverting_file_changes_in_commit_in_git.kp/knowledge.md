---
title: Undo modifications to a file in a commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To revert changes to a file in a commit in Git, use the `git revert` command.
---

**Contents**

[TOC]

# Revert a Single File in a Commit

1. Checkout the commit you want to revert:
   ```git checkout <commit_hash>```
2. Revert the file:
   ```git checkout <commit_hash> -- <file_name>```
3. Create a new commit with the reverted file:
   ```git commit -m "Reverted <file_name> to <commit_hash>"```

# Revert the Entire Commit

1. Checkout the commit you want to revert:
   ```git checkout <commit_hash>```
2. Revert the commit:
   ```git revert <commit_hash>```
3. Create a new commit with the reverted changes:
   ```git commit -m "Reverted <commit_hash>"```
