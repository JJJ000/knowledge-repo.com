---
title: What is the process for looking up a specific sequence of characters in text documents?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the regular expression module (re) and the os module to iterate through files in a directory and search for the string using re.search().
---

**Contents**

[TOC]

## Section 1: Introduction

In this tutorial, we will learn how to search for a string in text files using Python. Python provides various modules that can be used to read and handle different types of files. We will be using the `os` module to traverse a directory and the `re` module to search for the string in the text files.

## Section 2: Looking for Files in a Directory with the `os` module

To search for a string in text files, we need to traverse a directory and read each file. We can use the `os` module to traverse the directory and get a list of all the files. The `os` module also provides various functions to get information about the files in the directory. Here is an example of how to use the `os` module to get a list of all text files in a directory:

```python
import os

def get_files_in_directory(directory):
    file_list = []
    for path, subdirs, files in os.walk(directory):
        for name in files:
            if name.endswith(".txt"):
                file_list.append(os.path.join(path, name))

    return file_list

directory = 'path/to/directory'
files = get_files_in_directory(directory)
print(files)
```
This code returns a list of all text files in the given directory.

## Section 3: Searching a String in a Text File

Now that we have a list of all text files in the directory, we can read each file and search for the string in it. We can use the `re` module to search for the string in the file. Here is an example of how to search for a string in a text file:

```python
import re

def search_string_in_file(file_path, string):
    with open(file_path) as file:
        for line in file:
            if re.search(string, line):
                return True

    return False

string_to_search = "example_string"
for file in files:
    if search_string_in_file(file, string_to_search):
        print(f"{string_to_search} found in {file}")
    else:
        print(f"{string_to_search} not found in {file}")
```

This code reads each file in the list and searches for the given string in the file. If the string is found in the file, it prints that the string was found in the file. If the string is not found in the file, it prints that the string was not found in the file.

## Section 4: Conclusion

In this tutorial, we learned how to search for a string in text files using Python. We used the `os` module to traverse the directory and get a list of all text files in the directory. We also used the `re` module to search for the string in each text file. By combining these modules, we were able to search for a string in all text files in a directory.
