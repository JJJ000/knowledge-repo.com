---
title: Can you relocate/change the name of files in git while preserving their history?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, it is possible to move/rename files in Git and maintain their history by using the `git mv` command.
---

**Contents**

[TOC]

### Yes

Git does allow users to move and rename files while preserving the file's history. This is done by using the `git mv` command.

### How to Use `git mv`

The `git mv` command works similarly to the `mv` command in Unix. The syntax is `git mv <old-file-name> <new-file-name>`. This command will move the file from its old location to the new location and update the Git repository to reflect the changes.

### Advantages of Using `git mv`

Using `git mv` to move and rename files has several advantages. First, it allows users to keep track of the file's history and allows them to easily revert back to an earlier version if necessary. Second, it allows users to easily keep track of changes to the file's name and location. Finally, it allows users to easily collaborate with other users on the same project.

### Disadvantages of Using `git mv`

There are some disadvantages to using `git mv` to move and rename files. First, it can be difficult to keep track of all the changes if there are a large number of files being moved and renamed. Second, it can be difficult to keep track of the changes if the files are moved across multiple branches. Finally, it can be difficult to merge the changes if the files are moved across multiple branches.
