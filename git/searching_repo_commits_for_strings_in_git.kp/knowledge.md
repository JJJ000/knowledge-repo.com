---
title: What is the best way to find a specific string in all commits from both git and mercurial in a repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To search through all Git and Mercurial commits in the repository for a certain string, use the respective commands `git log` and `hg log` with the `-S <string>` option.
---

**Contents**

[TOC]

**Git**

1. Find Commits: 
   - Use the `git log` command to search through all commits in the repository. 
   - When searching for a certain string, use the `--grep` option to search for a specific string in the commit messages.

2. View Commits: 
   - After finding the commits you want to view, use the `git show` command to view the full commit message and the changes made in that commit.

**Mercurial**

1. Find Commits: 
   - Use the `hg log` command to search through all commits in the repository. 
   - When searching for a certain string, use the `--keyword` option to search for a specific string in the commit messages.

2. View Commits: 
   - After finding the commits you want to view, use the `hg diff` command to view the full commit message and the changes made in that commit.
