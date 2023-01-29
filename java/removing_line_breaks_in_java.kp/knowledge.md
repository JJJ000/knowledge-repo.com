---
title: What is the best way to eliminate line breaks from a file in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the BufferedReader.readLine() method to read the file line-by-line, and use the String.replaceAll() method to remove line breaks.
---

**Contents**

[TOC]

### Step 1: Read the File

Using a `BufferedReader` object, read the file line by line and store the content in a `StringBuilder` object.

### Step 2: Remove Line Breaks

Loop through the `StringBuilder` object and use the `replaceAll()` method to remove all line breaks (`\r` and `\n`).

### Step 3: Write to File

Write the modified content back to the file using a `BufferedWriter` object.

### Step 4: Close Resources

Close the `BufferedReader` and `BufferedWriter` objects to free up system resources.
