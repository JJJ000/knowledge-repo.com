---
title: What is the process for writing a string to a text file using java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the PrintWriter class to write a string to a text file.
---

**Contents**

[TOC]

### Create a FileWriter Object

The first step to save a String to a text file in Java is to create a FileWriter object. This object is used to write characters to a file. It is important to note that the FileWriter class should not be used to write raw bytes, as it uses the platform’s default character encoding.

### Write the String to the File

Once the FileWriter object has been created, the next step is to write the String to the file. This can be done using the write() method of the FileWriter object. This method takes a single argument, which is the String that needs to be written to the file.

### Close the FileWriter

Once the String has been written to the file, it is important to close the FileWriter object. This can be done using the close() method of the FileWriter object. This will ensure that all the data has been written to the file and that there are no open file handles.

### Flush the FileWriter

Finally, it is important to flush the FileWriter object. This can be done using the flush() method of the FileWriter object. This will ensure that all the data that has been written to the file is actually written to the file and not just stored in the FileWriter’s buffer.
