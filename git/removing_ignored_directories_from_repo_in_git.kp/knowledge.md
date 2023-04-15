---
title: Delete the directory from the remote repository after adding it to the .gitignore file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No, you cannot remove a directory from a remote repository after adding it to .gitignore.
---

**Contents**

[TOC]

### Deleting Directories from the Remote Repository

1. Remove the directory from the local repository:
   - Use the command `git rm -r <directory_name>` to delete the directory from the local repository.

2. Commit the changes:
   - Use the command `git commit -m "<message>"` to commit the changes to the local repository.

3. Push the changes to the remote repository:
   - Use the command `git push origin master` to push the changes to the remote repository.

4. Verify the changes on the remote repository:
   - Use the command `git ls-tree --full-tree -r <branch_name>` to verify that the directory has been removed from the remote repository.
