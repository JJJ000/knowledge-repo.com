---
title: What is the commit history for a single branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run the command `git log <branch\_name>`.
---

**Contents**

[TOC]

# Section 1: Checkout the Branch

In order to view the commit history for just one branch, you must first check out the branch. To do this, you can use the command `git checkout <branch_name>` where `<branch_name>` is the name of the branch you want to view the commit history for.

# Section 2: View the Commit History

Once you have checked out the branch, you can view the commit history for that branch by using the command `git log`. This will show a list of all the commits on the branch, with the most recent commit at the top.

# Section 3: View Commit Details

If you want to view more details about a particular commit, you can use the command `git show <commit_hash>` where `<commit_hash>` is the hash of the commit you want to view. This will show you the message, author, and date of the commit, as well as any changes that were made.

# Section 4: View Diff

If you want to view the changes made in a particular commit, you can use the command `git diff <commit_hash>` where `<commit_hash>` is the hash of the commit you want to view. This will show you a diff of the changes that were made in that commit.
