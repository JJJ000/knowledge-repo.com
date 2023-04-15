---
title: Git does not take into account the contents of the '.gitignore' file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Files and directories listed in .gitignore are not tracked or maintained by Git.
---

**Contents**

[TOC]

### What is .gitignore?

`.gitignore` is a file that is used to tell Git which files or directories should be ignored when performing operations such as committing or pushing. This file is usually found in the root directory of a repository.

### How is .gitignore used?

`.gitignore` is used to prevent certain files or directories from being tracked by Git. It is also used to prevent files that are specific to a certain environment or platform from being committed. For example, if a project contains files that are specific to a Windows environment, such as .dll files, these can be added to the `.gitignore` file so that they are not tracked by Git.

### What is ignored by .gitignore?

`.gitignore` can be used to ignore any file or directory that is not part of the project. This includes files such as log files, temporary files, and files that are specific to a certain environment or platform. It can also be used to ignore entire directories, such as the `node_modules` directory which contains all of the dependencies for a Node.js project.

### What is not ignored by .gitignore?

Files and directories that are explicitly mentioned in the `.gitignore` file will be tracked by Git. Additionally, files and directories that are not mentioned in the `.gitignore` file will also be tracked by Git. It is important to note that `.gitignore` only affects the files and directories that are in the same directory as the `.gitignore` file. Files and directories in subdirectories will not be affected by the `.gitignore` file.
