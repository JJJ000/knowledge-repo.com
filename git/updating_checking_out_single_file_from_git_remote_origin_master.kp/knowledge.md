---
title: How can I update or check out a single file from the remote origin master branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To update/checkout a single file from remote origin master, use the command `git checkout <remote> <branch> -- <path/to/file>`.
---

**Contents**

[TOC]

### Checkout a Single File from Remote Origin Master
1. Navigate to the directory of the file you want to checkout.
2. Run the command `git checkout origin/master -- <filename>`.

### Update a Single File from Remote Origin Master
1. Navigate to the directory of the file you want to update.
2. Run the command `git pull origin master <filename>`.
