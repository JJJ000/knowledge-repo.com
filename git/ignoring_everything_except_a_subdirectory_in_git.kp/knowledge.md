---
title: What is the command to have git ignore all files except those in a specific subdirectory?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use a .gitignore file to specify which files and directories should be ignored, excluding the subdirectory.
---

**Contents**

[TOC]

1. Add a `.gitignore` File
--------------------------
Create a `.gitignore` file in the root directory of your repository.

2. Exclude All Files
--------------------
Add a line to the `.gitignore` file that excludes all files. This line should be `*` (asterisk).

3. Include Subdirectory
-----------------------
Add a line to the `.gitignore` file that includes the subdirectory you want to keep. This line should be the path to the subdirectory, e.g. `subdirectory/`.

4. Commit Changes
-----------------
Commit the changes to the `.gitignore` file, and all files except the ones in the specified subdirectory will be ignored.
