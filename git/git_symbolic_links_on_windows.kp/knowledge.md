---
title: Create symbolic links with git on windows
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git symbolic links in Windows are supported with the use of Windows` mklink command.
---

**Contents**

[TOC]

### What are Git Symbolic Links?
Git symbolic links are a type of special file that allow users to reference a file or directory in another location. They are similar to Windows shortcuts, but they are stored in the repository and are tracked by Git.

### How to Create Git Symbolic Links?
Creating a Git symbolic link is fairly straightforward. First, create the directory or file that you want to link to. Then, use the `git add` command to add it to the repository. Finally, use the `git commit` command to commit the changes.

### Advantages of Git Symbolic Links
Git symbolic links provide a number of advantages. They allow users to reference files or directories in other locations, which can be useful for organizing large projects. Additionally, they are tracked by Git, so they can be used to track changes over time.

### Disadvantages of Git Symbolic Links
One of the main disadvantages of Git symbolic links is that they can be difficult to manage in Windows. Additionally, they are not compatible with some operating systems, such as Mac OS X. Finally, they can be difficult to troubleshoot if something goes wrong.
