---
title: What is the procedure for staging only a portion of a new file with git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `git add -p` command to stage only parts of a new file.
---

**Contents**

[TOC]

# Section 1: Create a Patch File
1. Make the changes to the file you want to stage. 
2. Use `git diff` to generate a patch file containing the changes.
3. Copy the output of `git diff` into a new file.

# Section 2: Apply the Patch File
1. Use `git apply` to apply the patch file to the repository.
2. Use the `--index` flag to stage the changes to the index.
3. Commit the changes.

# Section 3: Revert Unstaged Changes
1. Use `git reset` to reset the file to its original state.
2. Use the `--hard` flag to discard any unstaged changes.

# Section 4: Clean Up
1. Use `git clean` to remove any untracked files created by the patch.
2. Use the `-f` flag to force the removal of the untracked files.
