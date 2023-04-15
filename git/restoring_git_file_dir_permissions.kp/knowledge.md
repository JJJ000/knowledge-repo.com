---
title: What steps should be taken to reset the permissions of files and folders within git if they have been altered?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run the command `git reset --hard` to restore the permissions of files and directories within git.
---

**Contents**

[TOC]

### Check the Status of the File

Before attempting to restore the permissions of a file or directory, it is important to check the status of the file in order to determine if any changes have been made. This can be done by running the command `git status` in the terminal. This will display a list of files that have been modified, added, or deleted since the last commit. 

### Restore Permissions

Once the status of the file has been checked, the permissions can be restored by using the `git reset` command. This command will reset the permissions of the specified file to the state of the last commit. For example, if the file was originally set to be readable by all users, the command `git reset --chmod=644 <file_name>` will reset the permissions to the original state.

### Commit the Changes

Once the permissions have been restored, the changes should be committed in order to save the new state of the file. This can be done by running the command `git commit -m "Message"` where the message should describe the changes that have been made. This will commit the changes to the repository and ensure that the file has the correct permissions.

### Push the Changes

Finally, the changes should be pushed to the remote repository in order to ensure that all users have access to the updated version of the file. This can be done by running the command `git push origin master` which will push the changes to the remote repository. This will ensure that all users have access to the updated version of the file with the correct permissions.
