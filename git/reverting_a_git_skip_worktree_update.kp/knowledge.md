---
title: Revert changes made to a file using 'git update-index --skip-worktree'
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, you cannot undo the git update-index --skip-worktree command.
---

**Contents**

[TOC]

# Reverting the Skip-Worktree Flag

## Step 1: Check the Status

Before attempting to undo the skip-worktree flag, it is important to check the status of the repository to ensure that the desired files are being tracked. To check the status, use the command `git status`.

## Step 2: Unskip the Worktree

Once the status has been checked, use the command `git update-index --no-skip-worktree <file>` to unskip the worktree for the specified file.

## Step 3: Commit Changes

After the worktree has been unskipped, the changes must be committed with the command `git commit -m <message>`.

## Step 4: Push Changes

Finally, push the changes to the remote repository with the command `git push origin <branch>`.
