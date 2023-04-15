---
title: Git is asking me for a password
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git is likely asking for your SSH key passphrase or credentials for a remote repository.
---

**Contents**

[TOC]

### Troubleshooting

### Check Credentials

The first step is to check that the credentials you are using are correct. If you have recently changed your password, make sure to update the credentials stored in Git. To update the credentials stored in Git, run the following command: 

`git config --global user.name "Your Name"`

`git config --global user.email your@email.com`

### Check SSH Key

If you are using SSH to authenticate with Git, make sure the SSH key is properly configured. To check the SSH key configuration, run the following command: 

`ssh -T git@github.com`

If the SSH key is not configured properly, you will receive an error message.

### Check Git Configuration

If your credentials and SSH key are properly configured, check the Git configuration to make sure it is properly set up. To check the Git configuration, run the following command: 

`git config --list`

If any of the configuration settings are incorrect, make sure to update them.
