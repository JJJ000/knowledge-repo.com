---
title: What is preventing git from ignoring the specified file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The file may not be in the correct location for Git to ignore it, or the file may not be listed in the .gitignore file.
---

**Contents**

[TOC]

**Check File Path**
1. Verify the file path is correct. Git is case sensitive, so make sure the file path matches the case of the file name.
2. Check the file is in the correct directory. If the file is in a subdirectory, the path should include the subdirectory. 

**Check Gitignore File**
3. Verify the file is not already included in the .gitignore file. If the file is in the .gitignore file, Git will ignore it.
4. Check the syntax of the .gitignore file. Make sure the file path is formatted correctly.
