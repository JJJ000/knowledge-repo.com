---
title: Restoring deleted files
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To delete files from the staging area in Git, use the `git rm` command.
---

**Contents**

[TOC]

### Overview

Git is a version control system that allows users to track changes made to a file or set of files over time. It is widely used for software development and other version control purposes. One of the key features of Git is its ability to stage deleted files. This means that the deleted files can be tracked and managed in the same way as any other type of file.

### Staging Deleted Files

Staging deleted files in Git is a simple process. To begin, the user must delete the file from the working directory. This will make the file no longer visible in the file system. The user must then add the deleted file to the staging area by using the “git add” command. This will add the deleted file to the staging area, where it can be managed and tracked.

### Committing Deleted Files

Once the deleted file has been added to the staging area, it can be committed to the repository by using the “git commit” command. This will save the deleted file in the repository and make it available to other users. It is important to note that the deleted file will still be tracked in the repository, even though it is no longer visible in the file system.

### Reverting Deleted Files

If necessary, the user can also revert the deleted file back to its original state by using the “git checkout” command. This will restore the file to its original state, as it was before it was deleted. It is important to note that this command will not restore any changes that were made to the file after it was deleted.
