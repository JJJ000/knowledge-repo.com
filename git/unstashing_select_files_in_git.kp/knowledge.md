---
title: What is the procedure for retrieving specific files from a stash?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use `git stash show -p | git apply` to unstash only certain files.
---

**Contents**

[TOC]

### Stash Changes

Before you can unstash only certain files in Git, you must first stash the changes you want to unstash. To do this, you can use the command `git stash`. This will save all of your changes to a "stash" that you can access later.

### View Stashed Changes

Once you have stashed your changes, you can view them by using the command `git stash list`. This will show you a list of all of the changes that have been stashed.

### Unstash Specific Files

To unstash only certain files, you can use the command `git stash show <stash-name> -- <file-name>`, where `<stash-name>` is the name of the stash and `<file-name>` is the name of the file you want to unstash. This will show you the contents of the file you want to unstash.

### Apply Unstashed Changes

Once you have viewed the contents of the file you want to unstash, you can apply the changes by using the command `git stash apply <stash-name> -- <file-name>`. This will apply the changes from the specified file to your working directory.
