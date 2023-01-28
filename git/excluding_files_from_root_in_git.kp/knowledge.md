---
title: How can I prevent a file from being tracked by git when it is located in the root directory?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To exclude a file from the root folder in Git, use the `git update-index --assume-unchanged` command.
---

**Contents**

[TOC]

1.  **Checkout the File**
 
   To exclude a file from root folder in Git, first check out the file. This will ensure that the file is not tracked by Git.

2.  **Remove the File from the Git Index**

   After checking out the file, remove the file from the Git index. This will ensure that the file is not committed to the repository.

3.  **Add the File to the .gitignore File**

   Finally, add the file to the .gitignore file. This will ensure that the file is not tracked by Git in the future.

4.  **Commit the Changes**

   After adding the file to the .gitignore file, commit the changes. This will ensure that the file is excluded from the repository.
