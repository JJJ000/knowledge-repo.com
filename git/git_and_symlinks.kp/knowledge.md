---
title: What is the best way to configure git to track symbolic links?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git can follow symlinks by setting the `core.symlinks` configuration option to true.
---

**Contents**

[TOC]

# Setting Up Symbolic Links

1. Create the symlink: Use the `ln -s` command to create a symbolic link. This command takes two arguments: the source file and the destination file. The source file is the file you want to link to, and the destination is the location where the link should be created.

2. Verify the symlink: Use the `ls -l` command to verify that the symlink has been created. This command will list all files and directories in a directory, and it will also show any symlinks.

# Configuring Git to Follow Symlinks

1. Set the configuration option: Use the `git config` command to set the `core.symlinks` option to `true`. This will tell Git to follow symlinks when it is operating on files and directories.

2. Verify the configuration: Use the `git config --list` command to verify that the `core.symlinks` option is set to `true`.

# Testing the Configuration

1. Create a test file: Create a file in a directory that is tracked by Git.

2. Create a symlink to the test file: Use the `ln -s` command to create a symlink to the test file.

3. Verify the symlink: Use the `ls -l` command to verify that the symlink has been created.

4. Add the symlink to Git: Use the `git add` command to add the symlink to the Git repository.

5. Commit the changes: Use the `git commit` command to commit the changes to the Git repository.

6. Verify the commit: Use the `git log` command to verify that the symlink has been committed to the Git repository.
