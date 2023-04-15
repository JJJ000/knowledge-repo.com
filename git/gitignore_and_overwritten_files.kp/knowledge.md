---
title: '.gitignore' refers to a file which lists the names of files and folders that should not be tracked by the version control system.

"the following untracked working tree files would be overwritten by checkout" means that any files or folders in the working directory that have not been included in the version control system will be replaced with the files from the version control system when a checkout operation is performed
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The .gitignore file specifies which files and directories should be ignored by Git, while the `The following untracked working tree files would be overwritten by checkout` message warns that existing files in the working tree will be overwritten by the files in the branch being checked out.
---

**Contents**

[TOC]

### gitignore

The `.gitignore` file is used to tell Git which files or folders to ignore when committing changes to a repository. It is a list of file patterns to ignore. When Git sees a pattern listed in the `.gitignore` file, it will not add the matching files to the repository.

### The Following Untracked Working Tree Files

The message "The following untracked working tree files would be overwritten by checkout" is a warning message indicating that files in the working directory would be overwritten if you were to switch branches. This message is displayed when you try to switch branches and there are files in the working directory that are not tracked by Git. This is a warning to let you know that those files will be lost if you switch branches.
