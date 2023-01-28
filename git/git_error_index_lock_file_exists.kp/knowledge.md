---
title: Git - fatal error a file already exists at '/path/my_project/.git/index.lock', so it cannot be created
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: The index.lock file needs to be removed before a new repository can be created.
---

**Contents**

[TOC]

**Solution 1:**

1. Delete the existing lock file:
   Run the following command in the project directory:
   ```git
   rm -f .git/index.lock
   ```

**Solution 2:**

2. Check the status of the repository:
   Run the following command in the project directory:
   ```git
   git status
   ```
   If there are any changes that need to be committed or pushed, do so before proceeding with the next step.

**Solution 3:**

3. Check the processes running on the system:
   Run the following command in the terminal:
   ```git
   ps aux | grep git
   ```
   This will list all the processes related to git. If there are any processes still running, kill them using the `kill` command.

**Solution 4:**

4. Try again:
   After following the above steps, try running the command again and it should work.
