---
title: Clone a git repository using ssh
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Clone a repository over SSH by running `git clone ssh//git@example.com/path/to/repo.git`.
---

**Contents**

[TOC]

### Cloning a Repository Using SSH

### Step 1: Check for SSH Keys

Before cloning a repository, you should check to make sure you have an SSH key set up. You can check for existing keys by running `ls -al ~/.ssh` in your terminal. If you don't have any SSH keys yet, you can generate one by running `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`.

### Step 2: Add Your SSH Key to GitHub

Once you have generated an SSH key, you will need to add it to your GitHub account. You can do this by going to the SSH and GPG Keys page in your GitHub account settings.

### Step 3: Clone the Repository

Once you have added your SSH key to GitHub, you can clone the repository by running `git clone git@github.com:USERNAME/REPOSITORY.git`. Replace `USERNAME` and `REPOSITORY` with the appropriate values for your repository.

### Step 4: Configure Your Local Repository

Once you have cloned the repository, you should configure your local repository by running `git config --local user.name "Your Name"` and `git config --local user.email "your_email@example.com"`. This will ensure that all commits you make are associated with your GitHub account.
