---
title: What is the git commit that added a particular string to any branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git log -S <string> --source` to find the Git commit that introduced a string in any branch.
---

**Contents**

[TOC]

### Cloning the Repository
1. Navigate to the repository that contains the string you are looking for.
2. Clone the repository to your local machine using `git clone <repository_url>`.

### Finding the Commit
1. Run `git log` to view the commit history of the repository.
2. Search through the commit messages to find the commit that introduced the string.

### Viewing the Commit
1. Run `git show <commit_hash>` to view the details of the commit, including the changes it introduced.
2. Search through the changes to find the string you are looking for.

### Checking out the Branch
1. Run `git checkout <branch_name>` to switch to the branch where the commit was introduced.
2. Run `git log` to view the commit history of the branch.
3. Search through the commit messages to find the commit that introduced the string.
