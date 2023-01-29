---
title: What is the command to display all tags associated with a commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run the command `git tag --contains <commit>` to list all tags that contain a commit in Git.
---

**Contents**

[TOC]

#1 Using the Command Line

1. Navigate to the local repository.
2. Execute the command `git log --decorate --oneline --tags`. This will list all commits and their associated tags.

#2 Using a Graphical Interface

1. Open the repository in the chosen graphical interface.
2. Select the “Log” tab.
3. Check the “Show Tags” option.
4. All commits and their associated tags will be listed.
