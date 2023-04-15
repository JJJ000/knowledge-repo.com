---
title: Delete sensitive files and their associated commits from git's record
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Using the BFG Repo-Cleaner, you can remove sensitive files and their commits from Git history.
---

**Contents**

[TOC]

### Using BFG Repo-Cleaner

BFG Repo-Cleaner is a tool for removing large files and sensitive data from a Git repository history. It works by rewriting the repository's history to remove the unwanted data, while keeping the rest of the history intact.

### Steps

1. Install the BFG Repo-Cleaner.
2. Clone your repository with the `--mirror` option.
3. Run the BFG command to remove the files and commits you want to remove.
4. Push the changes to your remote repository.

### Benefits

Using BFG Repo-Cleaner has the following benefits:

- Quickly and easily remove large files and sensitive data from a Git repository history.
- Keeps the rest of the repository’s history intact.
- Easy to use and requires minimal setup.
