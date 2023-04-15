---
title: What is the process for monitoring updates on a git repository hosted remotely (on origin)?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git fetch origin` to check for changes on the remote (origin) Git repository.
---

**Contents**

[TOC]

### Step 1: Fetch changes from remote

To check for changes on a remote Git repository, the first step is to fetch any changes from the remote repository. This can be done by running the command `git fetch origin`. This command will fetch any changes from the remote repository and store them in the local repository.

### Step 2: Check for changes

After the changes have been fetched, the next step is to check for any changes that have been made. This can be done by running the command `git diff origin/master`. This command will compare the local repository with the remote repository and show any differences.

### Step 3: Pull changes

Finally, if there are any changes that need to be pulled, the command `git pull origin` can be used. This command will pull any changes from the remote repository and merge them with the local repository.
