---
title: What is the process for making a temporary directory/folder in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Files.createTempDirectory() method to create a temporary directory/folder in Java.
---

**Contents**

[TOC]

### Creating the Directory

In Java, the `java.nio.file.Files` class provides the ability to create a directory. To create a directory, the following code can be used:

```
Path tempDir = Files.createTempDirectory("temp");
```

### Deleting the Directory

Once the directory is no longer needed, it can be deleted with the `delete()` method of the `Files` class. To delete the directory, the following code can be used:

```
Files.delete(tempDir);
```

### Exceptions

It is important to handle exceptions when creating and deleting directories. The `createTempDirectory()` method may throw a `IOException` if an I/O error occurs. The `delete()` method may throw a `NoSuchFileException` if the directory does not exist.

### Example

The following example demonstrates how to create and delete a temporary directory in Java:

```
try {
    Path tempDir = Files.createTempDirectory("temp");
    // Do something with the directory
    Files.delete(tempDir);
} catch (IOException e) {
    e.printStackTrace();
}
```
