---
title: What is the command to modify my git username in the terminal?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run the command `git config --global user.name <your new username>` to change your Git username in terminal.
---

**Contents**

[TOC]

### Step 1: Find Current Username

1. Open Terminal.
2. Enter the command `git config --list` and press Enter.
3. Look for the entry `user.name`. The value next to it is your username.

### Step 2: Change Username

1. Enter the command `git config --global user.name "new_username"` and press Enter.
2. Replace `new_username` with the username you want.

### Step 3: Verify Username Change

1. Enter the command `git config --list` and press Enter.
2. Look for the entry `user.name`. The value next to it should be your new username.

### Step 4: Push Changes

1. Enter the command `git push` and press Enter.
2. Your changes should now be pushed with your new username.
