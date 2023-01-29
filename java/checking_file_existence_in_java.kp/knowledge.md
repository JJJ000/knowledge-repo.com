---
title: What is the process for determining if a file exists in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Files.exists() method to check if a file exists in Java.
---

**Contents**

[TOC]

### Using File Class
The `File` class of the `java.io` package can be used to check if a file exists.

### Syntax
The following syntax can be used to check if a file exists:
```
File file = new File(fileName);
boolean exists = file.exists();
```

### Example
The following example demonstrates how to check if a file exists:
```
File file = new File("example.txt");
boolean exists = file.exists();
if (exists) {
    System.out.println("File exists!");
} else {
    System.out.println("File does not exist.");
}
```
