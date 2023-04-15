---
title: What is the process for making a file and adding content to it?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To create and write to a file in Java, use the FileWriter class.
---

**Contents**

[TOC]

**Creating a File**

1. Use the `java.io.File` class to create a file object.
2. Use the `createNewFile()` method to create a new file.

**Writing to a File**

1. Use the `java.io.FileWriter` class to create a file writer object.
2. Use the `write(String)` method to write a string to the file.
3. Use the `flush()` method to flush the writer's buffer.
4. Use the `close()` method to close the writer.
