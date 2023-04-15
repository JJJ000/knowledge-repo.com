---
title: What is the procedure for deleting version control from a project that was cloned from git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git config --remove-section file` to remove version tracking from a project cloned from git.
---

**Contents**

[TOC]

1. Remove Version Tracking from the Local Repository

- Open the terminal application in the project directory
- Run the command `git rm -r --cached .`
- Run the command `git add .`

2. Remove Version Tracking from the Remote Repository

- Open the terminal application in the project directory
- Run the command `git push origin --delete <branch>`

3. Verify Version Tracking is Removed

- Open the terminal application in the project directory
- Run the command `git status`
- Verify that the output does not contain any changes to be committed
