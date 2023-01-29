---
title: What is the process for altering the default directory for git bash on windows?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can change the default location for Git Bash on Windows by changing the installation directory during the installation process.
---

**Contents**

[TOC]

### Step 1: Open Git Bash

Open Git Bash and type the following command:

```git
cd ~
```

This will take you to your home directory.

### Step 2: Create a New Directory

Create a new directory for your Git Bash default location. For example:

```git
mkdir git-bash
```

### Step 3: Change the Default Location

Type the following command to change the default location of Git Bash to the new directory you just created:

```git
git config --global core.gitbashdir /c/Users/<username>/git-bash
```

Replace `<username>` with your username.

### Step 4: Test the New Location

Type the following command to test the new location:

```git
cd git-bash
```

If you are now in the new directory, the default location has been successfully changed.
