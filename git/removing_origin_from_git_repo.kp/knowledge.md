---
title: How to delete a remote repository from git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git remote remove origin` to remove origin from the git repository.
---

**Contents**

[TOC]

### Delete the Origin Remote
1. To delete the origin remote, run `git remote remove origin` in the command line.

### Remove Origin from Git Config
1. To remove origin from the git config file, open the file in a text editor.
2. Find the line that says `[remote "origin"]` and delete it.

### Commit and Push Changes
1. After deleting the `origin` remote and removing it from the git config file, commit the changes and push them to the remote repository.

### Verify Changes
1. To verify that origin has been removed, run `git remote -v` in the command line. The output should not include any references to origin.
