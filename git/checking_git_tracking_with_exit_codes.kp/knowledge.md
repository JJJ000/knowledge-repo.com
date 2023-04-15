---
title: What is the shell exit code for determining if a file is tracked by git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git ls-files --error-unmatch <file>`; if the exit code is 0, the file is tracked, otherwise it is not.
---

**Contents**

[TOC]

### Checking File Status

The first step in determining if a file is tracked by git is to check the status of the file. To do this, you can use the `git status` command. This command will show the status of all files in the current working directory, including whether they are tracked by git or not.

### Parsing Output

The output of the `git status` command is a list of all files in the current directory and their status. You can parse this output to determine which files are tracked by git. To do this, you can use the `grep` command to search for lines containing the string "tracked" in the output.

### Checking Exit Code

The final step is to check the exit code of the `git status` command. If the command was successful, the exit code will be 0. If the command failed, the exit code will be non-zero. If the exit code is 0, then all of the files in the current directory are tracked by git.

### Conclusion

In conclusion, you can determine if a file is tracked by git by using the `git status` command and parsing the output. If the exit code of the command is 0, then all files in the current directory are tracked by git.
