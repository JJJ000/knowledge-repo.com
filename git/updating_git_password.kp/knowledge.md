---
title: What is the process for changing my git password?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git config --global user.password <new-password>` to update the password for Git.
---

**Contents**

[TOC]

### Updating the Password

### Step 1: Set up a New Password
First, you need to set up a new password for your Git account. This can be done by going to the "Settings" page in your Git account, and selecting the "Change Password" option. You will then be prompted to enter your new password twice. Make sure to remember the new password, as you will need it to access your Git account in the future.

### Step 2: Update the Remote
Once you have set up a new password for your Git account, you need to update the remote repository with the new password. To do this, you can use the `git remote` command. This command will allow you to update the remote repository with the new password.

### Step 3: Test the New Password
Once you have updated the remote repository with the new password, you need to test the new password to make sure it is working correctly. To do this, you can use the `git pull` command. This command will allow you to test the new password by attempting to pull from the remote repository. If the new password is working correctly, the pull will be successful.

### Step 4: Update Local Repository
Finally, you need to update your local repository with the new password. To do this, you can use the `git config` command. This command will allow you to update the local repository with the new password. Once you have done this, you will be able to access your Git account with the new password.
