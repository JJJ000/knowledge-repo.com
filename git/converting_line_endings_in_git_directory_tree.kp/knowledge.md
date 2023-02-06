---
title: Change the line endings for all files and folders in a directory tree using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git config --global core.autocrlf true` to convert line-endings for the entire directory tree.
---

**Contents**

[TOC]

# Section 1: Install dos2unix

dos2unix is a command-line tool that can be used to convert line-endings from Windows (CRLF) to Unix (LF). It is available for both Windows and Linux.

For Windows, you can download the binaries from their website and install them.

For Linux, you can install dos2unix using your package manager. For example, on Ubuntu you can use the command:

`sudo apt-get install dos2unix`

# Section 2: Convert Line-Endings

Once you have installed dos2unix, you can use it to convert line-endings for an entire directory tree.

The command you can use is:

`find <directory> -type f -exec dos2unix {} \;`

Where `<directory>` is the path to the directory you want to convert.

# Section 3: Add to Git

Once you have converted the line-endings, you will need to add the files to Git.

You can do this using the `git add` command. For example:

`git add <directory>`

This will add all the files in the specified directory to Git.

# Section 4: Commit Changes

Finally, you can commit the changes to Git using the `git commit` command.

For example:

`git commit -m "Convert line-endings to Unix"`

This will commit the changes to the repository with a message explaining what you have done.
