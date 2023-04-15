---
title: The command 'git' could not be found or recognized as an internal or external command
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git is not installed or is not added to the system PATH.
---

**Contents**

[TOC]

### Solution

### Install Git

The first step to resolving this error is to install git. Git is a version control system that allows users to keep track of changes made to files and collaborate with other users. To install git, visit the official Git website (https://git-scm.com/downloads) and download the appropriate version for your operating system.

### Set Path

Once git is installed, you will need to set the path to the directory where it is installed. To do this, open the Windows command prompt and type `set PATH=C:\Program Files\Git\bin`. This will add the path to the directory where git is installed.

### Verify Installation

Once the path has been set, you can verify that git is installed correctly by typing `git --version` in the command prompt. This will output the version of git that is installed on your system.

### Troubleshooting

If you are still having issues with git being recognized as a command, you may need to restart the computer and try again. If the issue persists, you may need to reinstall git or contact the support team for your operating system.
