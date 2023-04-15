---
title: The process of installing 'pip' is not successful due to an error message "oserror [errno 13] permission denied on directory"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run pip install command with sudo or run the command in administrator mode.
---

**Contents**

[TOC]

Section 1: Introduction

When working with Python, you may encounter a situation where you try to install a package using pip and receive an error message stating "OSError: [Errno 13] Permission denied on directory". This error message indicates that you do not have sufficient permissions to install the package in the specified directory.

In this article, we will explore the reasons why this error may occur and provide solutions on how to solve it.

Section 2: Reasons for the "OSError: [Errno 13] Permission denied on directory" error message 

There are several reasons why you may encounter this error message when trying to use pip to install a package. Some of these reasons include:

1. Insufficient permissions: You may not have sufficient permissions to install the package in the specified directory. This may be because you are not the owner of the directory or you do not have the necessary permissions to write to the directory.

2. Running pip as a standard user: If you are running pip as a standard user, you may encounter this error message if you do not have the necessary permissions to install packages system-wide. 

3. Running pip in a virtual environment: If you are running pip in a virtual environment, you may encounter this error message if you do not have the necessary permissions to write to the directory where the virtual environment is located.

Section 3: Solutions to the "OSError: [Errno 13] Permission denied on directory" error message 

There are several solutions that you can use to solve the "OSError: [Errno 13] Permission denied on directory" error message. Some of these solutions include:

1. Running pip as an administrator: If you are running pip from the command line, you can try running it as an administrator by opening the command prompt as an administrator and running the pip command from there.

2. Changing directory permissions: If the error message is caused by improper directory permissions, you can try changing the permissions on the directory to allow the current user to write to it.

3. Using a virtual environment: If you are running pip in a virtual environment, you can try creating the virtual environment in a directory where you have write permissions. You can also try creating a new virtual environment with the necessary permissions.

4. Setting pip user permissions: If you are running pip as a standard user, you can try setting pip user permissions by running the following command:

pip install --user package_name

This will install the package in the current user's home directory, which should have the necessary permissions to install packages.

Section 4: Conclusion 

The "OSError: [Errno 13] Permission denied on directory" error message is a common error that you may encounter when working with Python and pip. This error message can be caused by several factors, including insufficient permissions, running pip as a standard user, or running pip in a virtual environment.

We have provided several solutions that you can use to solve this error message, including running pip as an administrator, changing directory permissions, using a virtual environment, and setting pip user permissions. By following these solutions, you should be able to install the necessary packages using pip without encountering any permission-related errors.
