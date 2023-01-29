---
title: What is the Java code to determine the file extension of a file?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the getName() method of the File class to get the file extension.
---

**Contents**

[TOC]

1. Using the File Class

The File class provides the getName() method which returns the file name as a string. To get the file extension, we can use the substring method to extract the substring after the last occurrence of the dot (.) character.

2. Using the Path Class

The Path class provides the getFileName() method which returns the file name as a Path object. To get the file extension, we can use the toString() method to convert the Path object to a string, and then use the substring method to extract the substring after the last occurrence of the dot (.) character.

3. Using the FilenameUtils Class

The Apache Commons IO library provides the FilenameUtils class which contains the getExtension() method which returns the file extension as a string.

4. Using the URL Class

The URL class provides the getPath() method which returns the file name as a string. To get the file extension, we can use the substring method to extract the substring after the last occurrence of the dot (.) character.
