---
title: What is the procedure for locating and altering the original repository in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To find and change the origin/master in git, run the command `git remote -v` and then `git remote set-url origin <url>`.
---

**Contents**

[TOC]

### Finding the Origin/Master

To find the origin/master in git, you can use the command `git remote -v`. This will display the remote repository (origin/master) that is associated with your local repository. 

### Changing the Origin/Master

To change the origin/master in git, you can use the command `git remote set-url origin <url>`. This will change the remote repository (origin/master) associated with your local repository to the new URL that you provide.
