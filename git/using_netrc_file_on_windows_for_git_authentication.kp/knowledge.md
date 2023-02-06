---
title: Using a .netrc file on windows to store a git username and password
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: On Windows, the .netrc file can be used to save user and password by setting the file`s permissions to be readable only by the user.
---

**Contents**

[TOC]

# Section 1: Overview

Git is a distributed version control system that enables developers to collaborate on projects. It is widely used in software development and is the most popular version control system today. One way to make it easier to work with Git is to use a .netrc file. This file stores a user’s login credentials, so that they don’t have to type them in every time they want to access a repository. The .netrc file is especially useful on Windows, where the command line can be difficult to use.

# Section 2: Creating the .netrc File

The .netrc file is a plain text file that is stored in the user’s home directory. To create the file, open a text editor and save the file as “.netrc” (without the quotes) in the user’s home directory. The file should contain the following lines:

machine <hostname>
login <username>
password <password>

Replace <hostname>, <username>, and <password> with the appropriate values for the user.

# Section 3: Setting the File Permissions

Once the .netrc file has been created, it is important to set the file permissions correctly. The file should be set to read-only for the user, and no other users should be able to access it. To do this, open the command prompt and type the following command:

cacls <path_to_file> /E /P <username>:R

Replace <path_to_file> with the path to the .netrc file, and <username> with the user’s username.

# Section 4: Testing the .netrc File

Once the .netrc file has been created and the permissions have been set, it can be tested by attempting to clone a repository from the command line. If the .netrc file is set up correctly, the user should be able to clone the repository without having to enter their username and password.
