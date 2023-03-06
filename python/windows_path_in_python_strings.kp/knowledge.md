---
title: What is the correct format for including a windows path in a Python string literal?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use double backslashes to escape the path separators in a Windows path when writing it in a Python string literal.
---

**Contents**

[TOC]

Section 1: Introduction
When writing Python code that involves file paths on a Windows operating system, it is important to format the path correctly in order for the code to execute properly. In this guide, we will discuss how to write a Windows path in a Python string literal.

Section 2: Using backslashes in paths
In Windows, backslashes (\) are used to separate directories and subdirectories in file paths. However, backslashes are also used as escape characters in Python string literals. To avoid conflicts, we can use a double backslash (\\) in our Python string literal to represent a single backslash in the Windows file path. For example, if we want to reference a file at C:\Program Files\example\file.txt, we would write the path in our Python code as follows:

```python
path = "C:\\Program Files\\example\\file.txt"
```

Section 3: Using forward slashes in paths
Alternatively, we can use forward slashes (/) in our Python string literals to represent directory separators in the Windows file path. While this is not the standard convention in Windows file paths, Python can still recognize and interpret the path correctly. For example:

```python
path = "C:/Program Files/example/file.txt"
```

Section 4: Using raw strings
To simplify the process of writing Windows file paths in Python string literals, we can use a raw string. A raw string is a string literal with an "r" prefix that tells Python to interpret the string without any escape characters. This means that we can write a Windows file path exactly as it appears in the file system without having to worry about double backslashes or forward slashes. For example:

```python
path = r"C:\Program Files\example\file.txt"
```

By using a raw string, we can make our code easier to read and less error-prone when dealing with file paths on a Windows system.
