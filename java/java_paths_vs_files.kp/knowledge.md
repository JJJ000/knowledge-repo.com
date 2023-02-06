---
title: What is the difference between a Java path and a Java file?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Path is an abstract representation of a file system path, while File is a concrete representation of a file system path.
---

**Contents**

[TOC]

### Path
A `Path` object is a representation of a path to a file or directory. It is an abstraction of a file system path, and provides methods to get information about the path, such as its parent, root, and name components. It also provides methods to compare two paths, and to convert a path to a string.

### File
A `File` object represents a file or directory in the file system. It provides methods to read and write to the file, as well as methods to get information about the file, such as its size and last modified date. It also provides methods to list the contents of a directory, and to create and delete files and directories.
