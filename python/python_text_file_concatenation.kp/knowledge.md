---
title: What is the method to join text files in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To concatenate text files in Python, you can open all files in append mode and write the contents of one file into another.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, there are different ways to concatenate text files. The most common approach is to use built-in functions or modules in Python, such as the "open()" function and the "join()" method. In this article, we will discuss some of the most popular ways to concatenate text files in Python.

Section 2: Concatenating text files using the "open()" function
One way to concatenate text files in Python is to use the "open()" function. This function is used to open a file and return a file object that can be used to read or write data to the file. To concatenate two or more text files using the "open()" function, we can follow these steps:
1. Open a new file in write mode using the "open()" function.
2. Read the contents of the first file and write it to the new file.
3. Repeat step 2 for all the remaining files to be concatenated.
4. Close all the files.

Example:
```python
files = ["file1.txt", "file2.txt", "file3.txt"]
with open("output.txt", "w") as outfile:
    for f in files:
        with open(f, "r") as infile:
            outfile.write(infile.read())
```

Section 3: Concatenating text files using the "join()" method
Another way to concatenate text files in Python is to use the "join()" method. This method joins two or more strings or lists into a single string or list, respectively. To concatenate multiple text files using the "join()" method, we can follow these steps:
1. Read the contents of each file and store them as separate strings or lists.
2. Use the "join()" method to join all the strings or lists into a single string or list.
3. Write the concatenated string or list to a new file.

Example:
```python
files = ["file1.txt", "file2.txt", "file3.txt"]
contents = []
for f in files:
    with open(f, "r") as infile:
        contents.append(infile.read())
    
output = "".join(contents)
with open("output.txt", "w") as outfile:
    outfile.write(output)
```

Section 4: Conclusion
Concatenating text files in Python can be done using different techniques. In this article, we have discussed two popular ways to concatenate text files, using the "open()" function and the "join()" method. Both approaches are simple and easy to implement, and the choice between them depends on personal preference and the specific requirements of the task at hand.
