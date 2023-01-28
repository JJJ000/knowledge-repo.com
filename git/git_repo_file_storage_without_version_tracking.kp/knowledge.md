---
title: Store the file in a git repository, but do not monitor any alterations
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Create a .gitignore file to ignore changes to the file.
---

**Contents**

[TOC]

#1 Set Git to Ignore File

The first step to not tracking changes to a file in a Git repository is to set Git to ignore the file. This can be done by adding the file to the .gitignore file in the root of the repository.

#2 Avoid Committing File

Once the file is set to be ignored, it is important to avoid committing the file to the repository. This can be done by ensuring that the file is not included when running the `git add` command.

#3 Ignore File on All Branches

It is also important to ensure that the file is ignored on all branches of the repository. This can be done by adding the file to the .gitignore file on each branch.

#4 Monitor File Changes

Finally, it is important to monitor the file for any changes that may be made. This can be done by running the `git status` command to check for any changes to the file.
