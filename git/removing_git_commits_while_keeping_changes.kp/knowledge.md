---
title: What is the best way to delete certain commit log entries from a git repository while preserving their changes?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To remove selected commit log entries from a Git repository while keeping their changes, use the `git rebase -i` command.
---

**Contents**

[TOC]

# Section 1: Identify the Commits to be Removed

The first step in removing selected commit log entries from a Git repository while keeping their changes is to identify the commits to be removed. This can be done by using the `git log` command to view the commit history. The `git log` command will display the commit messages, the author, and the date and time of each commit. Once the commits to be removed have been identified, the commit hashes can be noted for later use.

# Section 2: Create a New Branch

The next step is to create a new branch from the current branch. This can be done using the `git checkout -b <new_branch_name>` command. This will create a new branch from the current branch and switch to it.

# Section 3: Revert the Commits

Once the new branch has been created, the commits to be removed can be reverted using the `git revert <commit_hash>` command. This command will revert the changes made in the specified commit and create a new commit with the changes. The `git revert` command can be used multiple times to revert multiple commits.

# Section 4: Merge the New Branch

Once the commits have been reverted, the new branch can be merged back into the original branch. This can be done using the `git merge <new_branch_name>` command. This will merge the changes from the new branch into the original branch. After the merge is complete, the new branch can be deleted.
