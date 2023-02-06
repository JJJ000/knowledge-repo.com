---
title: What is the process for creating aliases in git bash for windows?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In the Git Bash for Windows, aliases can be set by editing the .bashrc file in the user`s home directory.
---

**Contents**

[TOC]

## Step 1: Open the .bashrc File

In Git Bash, type the command `nano ~/.bashrc` to open the .bashrc file. The .bashrc file is a configuration file that contains settings for the Bash shell.

## Step 2: Add Alias

Once the .bashrc file is open, add an alias at the bottom of the file. The alias should follow this format: `alias <name>="<command>"`. For example, `alias gs="git status"`.

## Step 3: Save and Exit

Press `Ctrl+X` to exit the nano editor, then press `Y` to save the changes. 

## Step 4: Activate Alias

Type the command `source ~/.bashrc` to activate the alias. The alias can now be used in Git Bash.
