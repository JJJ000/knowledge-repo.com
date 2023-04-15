---
title: What is the most efficient way to read a large text file line by line using java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use a BufferedReader to read a large text file line by line in Java.
---

**Contents**

[TOC]

### Using a BufferedReader

The easiest way to read a large text file line by line using Java is to use a `BufferedReader`. This class is used to read text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines.

### Creating the BufferedReader

To create a `BufferedReader`, you need to pass a `FileReader` object to its constructor. The `FileReader` class is used to read characters from a file.

To create a `FileReader` object, you need to pass the file path to its constructor. The following code snippet creates a `BufferedReader` object from a file path:

```java
String filePath = "/path/to/file.txt";
BufferedReader br = new BufferedReader(new FileReader(filePath));
```

### Reading the File Line by Line

Once the `BufferedReader` object is created, you can read the file line by line using the `readLine()` method. This method returns a `String` object containing the contents of the line, or `null` if the end of the stream has been reached.

The following code snippet reads the file line by line and prints the contents of each line:

```java
String line;
while ((line = br.readLine()) != null) {
    System.out.println(line);
}
```

### Closing the BufferedReader

Once you are done reading the file, you should close the `BufferedReader` object to free up system resources. This can be done using the `close()` method.

The following code snippet closes the `BufferedReader` object:

```java
br.close();
```
