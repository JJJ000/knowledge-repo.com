---
title: What is the total number of git commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can get the Git commit count by running the command `git rev-list HEAD --count`.
---

**Contents**

[TOC]

### Using Git Log

1. Open a terminal window and navigate to the root directory of the repository.
2. Run the command `git log --oneline`.
3. Count the number of commits that are displayed.

### Using Git Count-Object

1. Open a terminal window and navigate to the root directory of the repository.
2. Run the command `git count-object -v`.
3. Look for the line that says `count:` followed by a number. This is the commit count.

### Using Git Shortlog

1. Open a terminal window and navigate to the root directory of the repository.
2. Run the command `git shortlog -sn`.
3. Count the number of commits that are displayed.

### Using Git Rev-List

1. Open a terminal window and navigate to the root directory of the repository.
2. Run the command `git rev-list HEAD --count`.
3. The output of the command will be the commit count.
