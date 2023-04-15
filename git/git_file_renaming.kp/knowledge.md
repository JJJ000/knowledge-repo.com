---
title: Managing file name changes in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git can track file renames by using the `git mv` command.
---

**Contents**

[TOC]

### Renaming a File

Renaming a file in Git is a straightforward process. First, use the command `git mv` to move the file to its new name. This command takes two arguments: the old file name and the new file name.

For example, if you wanted to rename `old_file.txt` to `new_file.txt`, you would use the command `git mv old_file.txt new_file.txt`.

### Committing the Change

Once you have renamed the file, you need to commit the change in order to save it in your repository. To do this, use the command `git commit -m` and include a message that describes the change you have made.

For example, if you had renamed `old_file.txt` to `new_file.txt`, you could use the command `git commit -m "Renamed old_file.txt to new_file.txt"`.

### Pushing the Change

Once you have committed the change, you need to push it to the remote repository. To do this, use the command `git push`. This will push the changes to the remote repository, making them available to all users who have access to the repository.

### Additional Considerations

It is important to note that renaming a file in Git does not delete the old file. The old file will still exist in the repository, but it will no longer be tracked by Git. If you wish to delete the old file, you will need to use the command `git rm` to remove it from the repository.
