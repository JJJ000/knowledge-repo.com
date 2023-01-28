---
title: View the commit history for a specific branch using git log
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git log --oneline --decorate --graph --all --branches [branch\_name]` to get commits only for a specific branch.
---

**Contents**

[TOC]

### Checkout the branch

Before checking out the branch, make sure you have the latest version of the branch with the command:

`git fetch`

Once the latest version of the branch is retrieved, you can check out the branch with the command:

`git checkout <branch-name>`

### View the Log

Once the branch is checked out, you can view the log of commits with the command:

`git log --oneline --decorate --graph`

This will display the log in a one-line format, with branch decorations and a graph of the commits.

### Filter the Log

You can further filter the log to show only the commits for the specific branch with the command:

`git log --oneline --decorate --graph <branch-name>`

### Show More Information

If you want to see more information about the commits, you can add the `--stat` flag to the log command:

`git log --oneline --decorate --graph --stat <branch-name>`
