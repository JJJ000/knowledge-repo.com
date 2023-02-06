---
title: Neglecting the contents of a directory that has already been logged in
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can ignore the contents of a checked-in directory by adding it to your .gitignore file.
---

**Contents**

[TOC]

##### Excluding a Directory

To exclude a directory from being tracked by Git, you can use the `.gitignore` file. This file is placed in the root of your repository and should contain a list of files and directories that should be ignored.

##### Ignoring an Already Checked-in Directory

If the directory is already checked-in to the repository, you can use the `git rm --cached` command to remove it from the repository and ignore it. This command will remove the directory from the repository but will keep it on the local machine.

##### Updating the .gitignore File

After excluding the directory from the repository, you should add it to the `.gitignore` file. This will ensure that the directory will not be added to the repository in the future.

##### Committing the Changes

Finally, you should commit the changes to the repository. This will ensure that the changes have been applied and the directory will remain excluded.
