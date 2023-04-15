---
title: What is the procedure for accessing a file from the resource folder?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the ClassLoader.getResource() method to load a file from the resource folder in Java.
---

**Contents**

[TOC]

### Locating the File

In order to load a file from a resource folder in Java, the file must first be located. This can be done by using the `getResource()` method or the `getResourceAsStream()` method.

### Using the getResource() Method

The `getResource()` method can be used to locate a file in the resource folder. This method takes a string argument which is the path to the file, relative to the resource folder. For example, if the file is located in the `resources/file.txt` folder, the following code can be used to retrieve the file:

```java
URL url = getClass().getResource("/resources/file.txt");
```

### Using the getResourceAsStream() Method

The `getResourceAsStream()` method can also be used to locate a file in the resource folder. This method takes a string argument which is the path to the file, relative to the resource folder. For example, if the file is located in the `resources/file.txt` folder, the following code can be used to retrieve the file:

```java
InputStream in = getClass().getResourceAsStream("/resources/file.txt");
```

### Reading the File

Once the file has been located, it can be read using the `InputStream` or `URL` objects. For example, the following code can be used to read the file using the `InputStream` object:

```java
BufferedReader reader = new BufferedReader(new InputStreamReader(in));
String line;
while ((line = reader.readLine()) != null) {
    System.out.println(line);
}
```
