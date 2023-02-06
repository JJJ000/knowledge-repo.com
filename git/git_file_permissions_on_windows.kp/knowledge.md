---
title: Change permissions for files on windows using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git file permissions on Windows are based on the underlying NTFS permissions.
---

**Contents**

[TOC]

# Section 1: File Permissions

On Windows, each file has three sets of permissions that can be set:

- Read: Allows users to view the contents of the file
- Write: Allows users to modify the contents of the file
- Execute: Allows users to execute the file

# Section 2: Git File Permissions

When using Git on Windows, the file permissions are set automatically based on the user's settings. The default permissions are Read and Write for all files, and Execute for executable files.

# Section 3: Changing File Permissions

It is possible to change the file permissions for Git files on Windows. This can be done by using the `git update-index` command. This command allows users to specify the permissions for each file, as well as set the default permissions for all files in the repository.

# Section 4: Recommended Practices

It is recommended that users only change the file permissions if absolutely necessary. If the default permissions are sufficient, it is best to leave them as-is to avoid any potential issues.
