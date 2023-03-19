---
title: What are the steps to generate a fully compressed tar file using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `tarfile` module in Python to create a tar file and then compress it using the `gzip`, `bz2`, or `lzma` module.
---

**Contents**

[TOC]

## Section 1: Introduction
Tar is an archive file format used to group multiple files or directories into a single file. The tar file format is commonly used in the Unix and Linux operating systems. In this article, we will learn how to create a compressed tar file using Python.

## Section 2: Creating a Tar File

To create a tar file, we can use the tarfile module in Python. It provides a high-level interface for creating, extracting, and manipulating tar archives. We can create a tar file using the following code:

```python
import tarfile

# create a tar file
with tarfile.open('example.tar', mode='w') as archive:
    archive.add('file1.txt')
    archive.add('file2.txt')
    archive.add('dir1')
```

In the above code, we created a tar file called example.tar using the tarfile.open() method. We specified the mode as 'w' to indicate that we want to create a new archive. We added three items to the archive using the archive.add() method. The method takes a file or directory path as an argument and adds it to the archive.

## Section 3: Compressing the Tar File

To compress the tar file, we can use one of the compression algorithms supported by the tarfile module. The supported compression algorithms are gzip, bz2, and xz. We can specify the compression algorithm by passing the appropriate value to the 'w' mode. For example, to create a gzipped compressed tar file, we can use the following code:

```python
import tarfile

# create a gzipped compressed tar file
with tarfile.open('example.tar.gz', mode='w:gz') as archive:
    archive.add('file1.txt')
    archive.add('file2.txt')
    archive.add('dir1')
```

In the above code, we changed the file name to example.tar.gz and specified the mode as 'w:gz' to indicate that we want to create a new archive with gzip compression. Similarly, we can use 'w:bz2' to create a bzip2 compressed tar file or 'w:xz' to create an xz compressed tar file.

## Section 4: Conclusion

In this article, we learned how to create a compressed tar file using Python. We used the tarfile module to create a tar file and specified the compression algorithm to create a compressed tar file. We can use this knowledge to create compressed archives of our files and directories in our Python programs.
