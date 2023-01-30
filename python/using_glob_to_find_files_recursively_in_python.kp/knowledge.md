---
title: What is the syntax for using glob() to search for files recursively?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The glob() function can be used to recursively search for files in a directory by using the asterisk (*) wildcard character.
---

**Contents**

[TOC]

# Section 1: Overview

The `glob()` function is a useful tool in Python for finding files and directories based on patterns of characters. It can be used to recursively search a directory tree for all files or directories matching a specified pattern.

# Section 2: Syntax

The syntax for the `glob()` function is as follows:

`glob.glob(pathname, recursive=True)`

Where `pathname` is the path to the directory you want to search and `recursive` is a Boolean value indicating whether or not to search subdirectories.

# Section 3: Examples

Here are some examples of using `glob()` to find files recursively:

To find all files in the current directory:
`glob.glob('*')`

To find all files in the current directory and its subdirectories:
`glob.glob('**/*')`

To find all files with the .txt extension in the current directory and its subdirectories:
`glob.glob('**/*.txt')`

# Section 4: Limitations

It is important to note that `glob()` does not support regular expressions, so you cannot use it to search for files with more complex patterns. Additionally, `glob()` does not support searching for files across multiple directories; instead, you must specify the directory and its subdirectories in the `pathname` argument.
