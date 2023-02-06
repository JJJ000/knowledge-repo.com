---
title: The command '__git_ps1' could not be found in the mac bash shell
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The \_\_git\_ps1 command is not available on Mac systems.
---

**Contents**

[TOC]

# Solution

## Check if git is installed

The first step is to check if git is installed on your Mac. If not, you can install it using the Homebrew package manager.

## Check if git-prompt.sh is installed

The second step is to check if the `git-prompt.sh` script is installed. This script provides the `__git_ps1` command, which is used to display the current git branch name in the terminal prompt.

## Install git-prompt.sh

If `git-prompt.sh` is not installed, you can install it by downloading it from the official git repository.

## Configure bash profile

Finally, you need to add the following line to your bash profile (`~/.bash_profile`):

```
source /path/to/git-prompt.sh
```

This will enable the `__git_ps1` command and you should no longer see the "command not found" error.
