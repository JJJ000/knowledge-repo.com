---
title: Search the history of a single file in git for a specific string
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To search for a string in a single file`s history, use the `git log -S <string>` command.
---

**Contents**

[TOC]

1. Prerequisites
-----------------
Before you can search for a string in a single file's history, you will need to have Git installed and have a repository set up with the file you want to search.

2. Finding the File
-------------------
To find the file you want to search, you can use the `git log` command to view the entire history of the repository. This will list all the commits in the repository, along with the files that were changed in each commit.

3. Searching the File
---------------------
Once you have identified the file you want to search, you can use the `git show` command to view the contents of the file in each commit. This will allow you to search for the string you are looking for in the file's history.

4. Limitations
--------------
It is important to note that the `git show` command only allows you to search for a string in the file's history at a single commit at a time. This means that if the string you are looking for has been changed or removed in subsequent commits, it will not be found.
