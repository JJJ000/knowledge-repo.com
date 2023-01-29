---
title: Retrieving a resource file from inside a jar
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A resource file can be read from within a jar file in Java using the getResourceAsStream() method.
---

**Contents**

[TOC]

### Accessing the Resource File

In order to access a resource file stored within a JAR file, the `getResourceAsStream()` method of the `Class` class can be used. The `getResourceAsStream()` method takes a String argument which is the full path of the resource file within the JAR file. 

### Example Code

The following code snippet shows an example of how to access a resource file stored within a JAR file.

```java
ClassLoader classLoader = getClass().getClassLoader();
InputStream inputStream = classLoader.getResourceAsStream("myResourceFile.txt");
```

### Reading the Resource File

Once the resource file is accessed, it can be read using the `InputStream` object. The `InputStream` class provides various methods which can be used to read the contents of the resource file. For example, the `read()` method can be used to read the contents of the resource file as a byte array.

### Closing the Resource File

Once the resource file has been read, it is important to close the `InputStream` object in order to release any resources associated with it. This can be done using the `close()` method of the `InputStream` class.
