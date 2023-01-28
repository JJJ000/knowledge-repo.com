---
title: What is the command to view previous commits using git blame?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git blame can be used to view the commit history for a specific line of code.
---

**Contents**

[TOC]

**Viewing Prior Commits with Git Blame**

1. Obtain the File's Commit History:
   To view prior commits with git blame, first obtain the file's commit history by running the command `git log <filename>`. This will list all of the commits that have been made to the file in reverse chronological order.

2. Run Git Blame:
   Next, run the command `git blame <filename>` to view the blame output for the file. This will list each line of the file and the commit that last modified it.

3. View Commit Details:
   To view the details of a particular commit, run the command `git show <commit-hash>`. This will display the commit message and the changes that were made in the commit.

4. View Diff of Commit:
   To view the diff of a particular commit, run the command `git diff <commit-hash>`. This will show the differences between the current version of the file and the version at the time of the commit.
