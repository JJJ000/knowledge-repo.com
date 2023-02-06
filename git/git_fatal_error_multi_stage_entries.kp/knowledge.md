---
title: Receiving a fatal error when attempting to commit multiple stages in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The error is caused by attempting to add multiple entries to the same stage in the same commit.
---

**Contents**

[TOC]

# Solution

## Step 1: Check the Git Config File
The first step to troubleshoot this issue is to check the git config file. This file is located in the `.git` directory of the repository.

## Step 2: Check for Multiple Stage Entries
The next step is to check for multiple stage entries in the `.git/config` file. If there are multiple entries, then this could be the cause of the fatal error.

## Step 3: Remove Unnecessary Entries
If multiple entries are found, then it is necessary to remove the unnecessary entries. This can be done by deleting the lines containing the entries from the `.git/config` file.

## Step 4: Restart Git
Finally, restart git to ensure that the changes take effect. This can be done by running the command `git reset --hard` in the terminal.
