---
title: Update email address in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run the command `git config --global user.email <new email>` to change the email address in Git.
---

**Contents**

[TOC]

### Change Email Address in the Global Configuration

1. Open the command line and navigate to the directory where your Git repository is located. 
2. Type `git config --global user.email "your_new_email@example.com"` and press enter. 
3. Your new email address will be set in the global configuration.

### Change Email Address in the Local Configuration

1. Open the command line and navigate to the directory where your Git repository is located. 
2. Type `git config user.email "your_new_email@example.com"` and press enter. 
3. Your new email address will be set in the local configuration.

### Verify the New Email Address

1. Open the command line and navigate to the directory where your Git repository is located. 
2. Type `git config --list` and press enter. 
3. The new email address should be displayed in the list of configurations.

### Push the Changes

1. Open the command line and navigate to the directory where your Git repository is located. 
2. Type `git push` and press enter. 
3. Your changes will be pushed with the new email address.
