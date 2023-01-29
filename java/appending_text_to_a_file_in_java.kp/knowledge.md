---
title: What is the process for adding text to an existing file in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the FileWriter class to append text to an existing file in Java.
---

**Contents**

[TOC]

### Using PrintWriter

Using the PrintWriter class, you can append text to an existing file in Java. To do this, the constructor of the PrintWriter class takes a FileWriter object as a parameter. This FileWriter object can be created by passing the file path and a boolean parameter to the FileWriter constructor. The boolean parameter should be set to true to enable appending. 

### Using BufferedWriter

Using the BufferedWriter class, you can also append text to an existing file in Java. To do this, the constructor of the BufferedWriter class takes a FileWriter object as a parameter. This FileWriter object can be created by passing the file path and a boolean parameter to the FileWriter constructor. The boolean parameter should be set to true to enable appending.

### Using FileWriter

Using the FileWriter class, you can also append text to an existing file in Java. To do this, you need to pass the file path and a boolean parameter to the FileWriter constructor. The boolean parameter should be set to true to enable appending.

### Writing to the File

Once you have created the PrintWriter, BufferedWriter, or FileWriter object, you can write to the file using the write() method. This method takes a string as a parameter, which is the text that you want to append to the existing file.
