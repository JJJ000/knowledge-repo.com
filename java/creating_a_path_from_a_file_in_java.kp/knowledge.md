---
title: Obtain a java.nio.file.path object from a java.io.file
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the File.toPath() method to get a java.nio.file.Path object from a java.io.File.
---

**Contents**

[TOC]

**Section 1: Overview**

Java.nio.file.Path is an object that encapsulates a platform-independent file system path. It is a part of Java NIO (New IO) package which was introduced in Java 7. It provides methods to access and manipulate files and directories. On the other hand, java.io.File is a class that represents a file or directory pathname. It is an older class that has been around since Java 1.0.

**Section 2: Difference between Path and File**

The main difference between Path and File is that Path is an interface and File is a class. Path provides methods to access and manipulate files and directories, while File provides methods to access and manipulate file and directory paths. Path also provides methods to access file attributes and operations on files, while File does not.

**Section 3: How to get Path from File**

The java.nio.file.Paths class provides a static method to get a Path object from a File object. The method is called Paths.get(File f). This method takes a File object as an argument and returns a Path object.

**Section 4: Example**

Here is an example of how to get a Path object from a File object:

```
File file = new File("/path/to/file");
Path path = Paths.get(file);
```
