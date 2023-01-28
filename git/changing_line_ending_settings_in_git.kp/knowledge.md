---
title: What are the steps to modify line-ending settings?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run the command `git config --global core.autocrlf <setting>` to change the line-ending settings in Git.
---

**Contents**

[TOC]

### Using .gitattributes

Git allows you to set line-ending settings on a per-repository basis by using a special file called `.gitattributes`. This file allows you to specify which line-endings should be used for each file in the repository. To set the line-ending settings, create a `.gitattributes` file in the root of your repository and add the following lines:

```git
* text=auto
*.sh eol=lf
```

This will set all text files to use the line-ending settings that are appropriate for the platform the file is checked out on, and all `.sh` files to use Unix-style line endings (LF).

### Using the `core.eol` Setting

Git also allows you to set the line-ending settings for the entire repository in the `.git/config` file. To do this, add the following line to the `[core]` section of the `.git/config` file:

```git
core.eol = lf
```

This will set all files in the repository to use Unix-style line endings (LF).

### Using the `git config` Command

You can also set the line-ending settings for the entire repository using the `git config` command. To do this, run the following command:

```git
git config --global core.eol lf
```

This will set all files in the repository to use Unix-style line endings (LF).
