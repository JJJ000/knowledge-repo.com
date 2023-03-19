---
title: What is the method for conducting a recursive sub-folder search and generating a list of files?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use os.walk() function to recursively search sub-folders and append the files to a list.
---

**Contents**

[TOC]

## Section 1: Setting Up the Recursive Function

To search for files recursively in Python, we can use a function that starts searching from a base directory and looks for sub-directories and files within it. We can use the `os` library to interact with the file system and check if a given path is a directory or a file. Here's an example of how to set up the recursive function:

```python
import os

def search_files(directory):
    file_list = []
    for root, dirs, files in os.walk(directory):
        for file in files:
            filepath = os.path.join(root, file)
            file_list.append(filepath)
    return file_list
```

In this code, we use the `os.walk` function to recursively traverse the directory tree rooted at `directory`. The function returns a generator that yields a tuple of three values at each iteration: the current directory name, a list of sub-directory names, and a list of file names. We iterate over the files list and add each file's path to our `file_list` variable.


## Section 2: Filtering Files by Extension

The function we created in Section 1 will return a list of all files in the directory tree regardless of their extension. If we want to filter the files based on some specific extension, we can add an `if` statement to our loop that checks the file extension. Here's an example:

```python
def search_files(directory, extension):
    file_list = []
    for root, dirs, files in os.walk(directory):
        for file in files:
            if file.endswith(extension):
                filepath = os.path.join(root, file)
                file_list.append(filepath)
    return file_list
```

In this code, we added an `if` statement that checks if the file name ends with the given `extension`. If it does, we add the file path to our `file_list`. We can now call the function with a specific extension:

```python
files = search_files('/path/to/folder', '.txt')
```

This will return a list of all `*.txt` files in the directory tree.


## Section 3: Ignoring Directories and Hidden Files

There may be cases where we want to exclude certain directories or files from the search. For example, we may want to ignore hidden files or folders or folders that match a specific pattern. We can do this by adding conditions to our search function. Here's an example:

```python
def search_files(directory, extension):
    file_list = []
    ignore = {'.git', '.idea', '__pycache__'}
    for root, dirs, files in os.walk(directory):
        # Exclude hidden directories and those in ignore list
        dirs[:] = [d for d in dirs if not d.startswith('.') and d not in ignore]
        for file in files:
            if not file.startswith('.') and file.endswith(extension):
                filepath = os.path.join(root, file)
                file_list.append(filepath)
    return file_list
```

In this code, we created a `ignore` set that contains folder names we want to exclude from the search. We use this set to filter out directories in the `os.walk` generator by reassigning the `dirs` variable to a filtered list. We also added a check to exclude hidden files. We can now call the function as before, and it will ignore the specified folders and hidden files.


## Section 4: Putting It All Together

We can now put all the previous sections together to create a function that can search recursively, filter by extension, and ignore directories and files. Here's the final code:

```python
import os

def search_files(directory, extension):
    file_list = []
    ignore = {'.git', '.idea', '__pycache__'}
    for root, dirs, files in os.walk(directory):
        # Exclude hidden directories and those in ignore list
        dirs[:] = [d for d in dirs if not d.startswith('.') and d not in ignore]
        for file in files:
            if not file.startswith('.') and file.endswith(extension):
                filepath = os.path.join(root, file)
                file_list.append(filepath)
    return file_list
```

Now we can call this function and get a list of all the files in the directory tree that match a specific extension and exclude hidden files and folders: 

```python
files = search_files('/path/to/folder', '.txt')
``` 

This code will return a list of all `*.txt` files in the directory tree, excluding hidden files and folders and those in the `ignore` set.
