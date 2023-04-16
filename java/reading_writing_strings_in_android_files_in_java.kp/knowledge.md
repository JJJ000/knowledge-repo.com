---
title: Write and read strings from/to a file on android
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To read/write a String from/to a file in Android in Java, use the FileInputStream/FileOutputStream classes.
---

**Contents**

[TOC]

#Section 1: Writing a String to a File

The following code snippet shows how to write a string to a file in Android.

```java
String filename = "myfile.txt";
String fileContents = "This is the content of my file.";
FileOutputStream outputStream;

try {
  outputStream = openFileOutput(filename, Context.MODE_PRIVATE);
  outputStream.write(fileContents.getBytes());
  outputStream.close();
} catch (Exception e) {
  e.printStackTrace();
}
```

#Section 2: Reading a String from a File

The following code snippet shows how to read a string from a file in Android.

```java
String filename = "myfile.txt";
String fileContents;
FileInputStream inputStream;

try {
  inputStream = openFileInput(filename);
  int size = inputStream.available();
  byte[] buffer = new byte[size];
  inputStream.read(buffer);
  inputStream.close();
  fileContents = new String(buffer);
} catch (Exception e) {
  e.printStackTrace();
}
```
