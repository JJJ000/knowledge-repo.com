---
title: What is the best way to use git diff for lines with a lot of text?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `--word-diff` flag to show the difference between long lines in git diff.
---

**Contents**

[TOC]

1. Check for Unstaged Changes
-------------------------
Git diff allows you to compare any two versions of a file to check for differences. This is especially useful when dealing with long lines of text. To check for unstaged changes, use the command `git diff` followed by the file name. This will show you the differences between the modified file and the version of the file stored in the repository.

2. Check for Staged Changes
-------------------------
If you have already staged changes to the file, you can use `git diff --staged` followed by the file name to compare the staged version of the file with the version in the repository. This will show you the differences between the two versions.

3. Check for Committed Changes
-----------------------------
To check for differences between two committed versions of a file, use the command `git diff <commit1> <commit2>` followed by the file name. This will show you the differences between the two versions of the file that have been committed to the repository.

4. Check for Uncommitted Changes
-------------------------------
If you want to compare two versions of a file that have not yet been committed, you can use the command `git diff HEAD` followed by the file name. This will show you the differences between the version of the file stored in the repository and the version of the file currently being worked on.
