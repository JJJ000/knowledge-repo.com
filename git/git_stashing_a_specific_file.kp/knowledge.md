---
title: What is the process for stashing a particular file using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can git stash a specific file by using the command `git stash push <file name>`.
---

**Contents**

[TOC]

### Step 1: Checkout to a New Branch

1. Create a new branch and check it out:
   ```
   git checkout -b <branch_name>
   ```

### Step 2: Stash the File

2. Stash the specific file:
   ```
   git stash push <file_name>
   ```

### Step 3: Checkout to the Original Branch

3. Checkout back to the original branch:
   ```
   git checkout <original_branch_name>
   ```

### Step 4: Pop the Stashed File

4. Pop the stashed file to the original branch:
   ```
   git stash pop
   ```
