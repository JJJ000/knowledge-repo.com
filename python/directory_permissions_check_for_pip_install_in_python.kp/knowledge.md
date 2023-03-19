---
title: Kindly verify the proprietorship and authorizations of the specified directory for the 'pip install' command
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The error message `Please check the permissions and owner of that directory` in Python`s pip install indicates that the user does not have sufficient permissions to access or modify the directory where pip is trying to install the package.
---

**Contents**

[TOC]

## Introduction

When using the `pip` command to install packages in Python, you may encounter an error message that says "Please check the permissions and owner of that directory". This error message indicates that there are issues with the file permissions of the directory in which you are trying to install the package. In this article, we will explain what causes this error and how to fix it. 

## Understanding file permissions

File permissions determine who can read, write, and execute files on the operating system. For example, when installing a package using pip, the user executing the command needs to have write permissions in the directory where the package is being installed. Otherwise, you will get the "Please check the permissions and owner of that directory" error message. 

The file permissions are denoted by a set of three letters: r (read), w (write) and x (execute). Each letter indicates whether a particular permission is granted or denied. 

## Checking file permissions

To check the permissions of a file or directory, you can use the `ls -l` command in the terminal. This will list all the files in the current directory, along with their permissions.

For example:
```
$ ls -l /path/to/directory
```

This will list the files and directories in `/path/to/directory`, along with their permissions.

## Changing file permissions

You can change file permissions using the `chmod` command.

For example, to grant write permission to the owner of a file, you can use the following command:
```
$ chmod u+w /path/to/file
```

Here, `u` denotes the owner of the file, and `+w` grants write permission.

To grant write permission to everyone, you can use the following command:
```
$ chmod a+w /path/to/file
```

Here, `a` denotes everyone (i.e., all users), and `+w` grants write permission. 

## Conclusion

In this article, we explained the "Please check the permissions and owner of that directory" error message that can occur when using pip to install packages in Python. We also showed how to check and change file permissions using the `ls` and `chmod` commands, respectively. By following these instructions, you can fix the error and successfully install Python packages using pip.
