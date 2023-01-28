---
title: Check out an older version of a file using git and save it with a different name
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the `git checkout` command with the <revision> and <file> parameters, followed by the `-b <new\_branch\_name>` parameter to create a new branch with the older revision of the file under a new name.
---

**Contents**

[TOC]

### Getting the Older Revision of a File

To get the older revision of a file, you can use the `git checkout` command. This command allows you to switch between different versions of a file.

### Specifying the Revision

When using the `git checkout` command, you can specify the revision of the file you want to get by using its commit hash. This is a unique identifier for each commit, and can be found in the output of the `git log` command.

### Checkout Under a New Name

If you want to checkout the older revision of a file under a new name, you can use the `-b` option. This will create a new branch with the specified name and checkout the file from the specified revision.

### Example

For example, if you wanted to checkout an older revision of a file named 'myfile.txt' under the name 'oldfile.txt', you could use the following command:

`git checkout -b oldfile.txt <commit-hash> myfile.txt`
