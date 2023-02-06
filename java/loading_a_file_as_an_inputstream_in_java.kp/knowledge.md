---
title: Various methods of obtaining an inputstream from a file
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The InputStream can be loaded from a File, URL, ByteArrayInputStream, FileInputStream, ObjectInputStream, PipedInputStream, SequenceInputStream, StringBufferInputStream, and DataInputStream.
---

**Contents**

[TOC]

### FileInputStream
This is the most basic way to load a file as an InputStream. The FileInputStream class is part of the java.io package and takes a File object as its parameter.

```java
File file = new File("path/to/file");
FileInputStream inputStream = new FileInputStream(file);
```

### BufferedInputStream
Using the BufferedInputStream class, you can wrap an existing InputStream and read data from it in chunks. This can be useful for performance reasons, as it reduces the number of times the underlying InputStream needs to be accessed.

```java
File file = new File("path/to/file");
FileInputStream inputStream = new FileInputStream(file);
BufferedInputStream bufferedInputStream = new BufferedInputStream(inputStream);
```

### FileReader
The FileReader class can also be used to load a file as an InputStream. It is part of the java.io package and takes a File object as its parameter.

```java
File file = new File("path/to/file");
FileReader inputStream = new FileReader(file);
```

### URL
The URL class can be used to load a file from a URL as an InputStream. It is part of the java.net package and takes a URL string as its parameter.

```java
String urlString = "http://example.com/file.txt";
URL url = new URL(urlString);
InputStream inputStream = url.openStream();
```
