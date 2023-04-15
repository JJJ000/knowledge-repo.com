---
title: What is the syntax for joining paths in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The java.nio.file.Paths class provides a static method called `resolve` which can be used to combine multiple paths into a single path.
---

**Contents**

[TOC]

### Using File.separator

The `File.separator` is a static string field in the `File` class, which is used to separate different parts of a file path. This is the recommended way to combine paths in Java.

The syntax for combining paths is as follows:

```java
String path = path1 + File.separator + path2;
```

Where `path1` and `path2` are the two paths to be combined.

### Using Paths.get

The `Paths.get()` method is another way to combine paths in Java. This method takes two paths as arguments and returns a `Path` object that represents the combined path.

The syntax for combining paths is as follows:

```java
Path path = Paths.get(path1, path2);
```

Where `path1` and `path2` are the two paths to be combined.

### Using File.toPath

The `File.toPath()` method is another way to combine paths in Java. This method takes a `File` object as an argument and returns a `Path` object that represents the combined path.

The syntax for combining paths is as follows:

```java
Path path = File.toPath(file1).resolve(file2);
```

Where `file1` and `file2` are the two files to be combined.

### Using String.join

The `String.join()` method is a useful utility for combining paths in Java. This method takes a delimiter string and an array of strings as arguments and returns a single string that is the concatenation of the array elements separated by the delimiter.

The syntax for combining paths is as follows:

```java
String path = String.join(File.separator, path1, path2);
```

Where `path1` and `path2` are the two paths to be combined.
