---
title: What is the most efficient method of displaying Java files in order of date modified?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The best way to list files in Java, sorted by Date Modified is to use the Files.list() method with a Comparator to sort the files by their last modified date.
---

**Contents**

[TOC]

## Using File Class
The File class provides a method called `listFiles()` which returns an array of files and directories in the directory. This array can be sorted using the `Arrays.sort()` method by passing a custom Comparator. The custom Comparator can compare the `lastModified()` values of the files and directories.

## Using FileVisitor
The FileVisitor interface provides a method called `preVisitDirectory()` which is called when a directory is visited. This method can be used to sort the files and directories in the directory based on the `lastModified()` values.

## Using PathMatcher
The PathMatcher interface provides a method called `matches()` which is used to match a file or directory based on the given criteria. This method can be used to sort the files and directories in the directory based on the `lastModified()` values.

## Using Streams
The Streams API provides a method called `sorted()` which can be used to sort the files and directories in the directory based on the `lastModified()` values. The Streams API also provides other methods such as `filter()` and `map()` which can be used to filter and map the files and directories in the directory.
