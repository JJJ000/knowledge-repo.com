---
title: Error when attempting to push to git unable to delete existing file (permission denied)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The error is likely due to not having permission to delete the old file.
---

**Contents**

[TOC]

# Solution 1: Change File Permissions

This error occurs when the user does not have the necessary permissions to overwrite the existing file. To fix this, the user needs to change the file permissions. This can be done by running the following command in the terminal:

```
chmod +x <filename>
```

This will give the user the necessary permissions to overwrite the existing file.

# Solution 2: Use sudo Command

If changing the file permissions does not work, the user can try using the `sudo` command to execute the `git push` command. This will give the user the necessary permissions to overwrite the existing file. The command to be used is as follows:

```
sudo git push
```

# Solution 3: Use Git Config

The user can also use the `git config` command to set the necessary permissions for the user to overwrite the existing file. The command to be used is as follows:

```
git config --global core.filemode false
```

This will set the necessary permissions for the user to overwrite the existing file.

# Solution 4: Use Git Clean

The user can also use the `git clean` command to clean the repository and remove any unnecessary files. This will allow the user to overwrite the existing file. The command to be used is as follows:

```
git clean -f
```

This will remove any unnecessary files and allow the user to overwrite the existing file.
