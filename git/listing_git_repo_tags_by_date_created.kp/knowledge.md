---
title: What is the command to display all tags in my git repository in chronological order of their creation?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git tag --list --sort=-creatordate`.
---

**Contents**

[TOC]

##### Using Git Log
1. Open the terminal and navigate to the directory containing your Git repository. 
2. Run the command `git log --pretty="%d" --decorate` to list all tags in your repository by the date they were created. 

##### Using Git Tag
1. Open the terminal and navigate to the directory containing your Git repository. 
2. Run the command `git tag --list --sort=creatordate` to list all tags in your repository by the date they were created.
