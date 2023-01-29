---
title: Converting a byte array to a file in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Files.write() method to write a byte array to a file in Java.
---

**Contents**

[TOC]

### Section 1 - Using FileOutputStream

FileOutputStream is a class from the Java IO package that can be used to write a byte array to a file. The following code snippet shows how to use FileOutputStream to write a byte array to a file:

```java
// Create a new FileOutputStream
FileOutputStream fos = new FileOutputStream("myFile.txt");

// Create a byte array
byte[] myByteArray = {1, 2, 3};

// Write the byte array to the file
fos.write(myByteArray);

// Close the FileOutputStream
fos.close();
```

### Section 2 - Using Files.write()

The Files class from the Java NIO package provides a write() method that can be used to write a byte array to a file. The following code snippet shows how to use Files.write() to write a byte array to a file:

```java
// Create a byte array
byte[] myByteArray = {1, 2, 3};

// Write the byte array to the file
Path path = Paths.get("myFile.txt");
Files.write(path, myByteArray);
```

### Section 3 - Using BufferedOutputStream

BufferedOutputStream is a class from the Java IO package that can be used to write a byte array to a file. The following code snippet shows how to use BufferedOutputStream to write a byte array to a file:

```java
// Create a new BufferedOutputStream
BufferedOutputStream bos = new BufferedOutputStream("myFile.txt");

// Create a byte array
byte[] myByteArray = {1, 2, 3};

// Write the byte array to the file
bos.write(myByteArray);

// Close the BufferedOutputStream
bos.close();
```

### Section 4 - Using FileChannel

FileChannel is a class from the Java NIO package that can be used to write a byte array to a file. The following code snippet shows how to use FileChannel to write a byte array to a file:

```java
// Create a new FileChannel
FileChannel channel = new FileChannel("myFile.txt");

// Create a byte array
byte[] myByteArray = {1, 2, 3};

// Write the byte array to the file
ByteBuffer buffer = ByteBuffer.wrap(myByteArray);
channel.write(buffer);

// Close the FileChannel
channel.close();
```
