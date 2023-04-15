---
title: Retrieving data from a plain text file using java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To read a plain text file in Java, use the FileReader class and the BufferedReader class to read the file line by line.
---

**Contents**

[TOC]

### Setting Up

In order to read a plain text file in Java, you will need to create a `FileReader` object. This object will allow you to read from a file.

### Creating a FileReader Object

To create a `FileReader` object, you will need to pass the path of the file you wish to read as an argument. For example:

```
FileReader fr = new FileReader("/path/to/file.txt");
```

### Reading the File

Once you have created the `FileReader` object, you can use the `read()` method to read the contents of the file. This method takes no arguments and returns an `int` which is the ASCII value of the character read.

### Closing the File

Once you have finished reading the file, it is important to close the `FileReader` object. This can be done using the `close()` method.

```
fr.close();
```
