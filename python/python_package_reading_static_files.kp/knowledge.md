---
title: What is the process of reading a (static) file from a Python package?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the package`s built-in `pkg\_resources` module with the path to the file as an argument.
---

**Contents**

[TOC]

## Introduction
Reading a static file from inside a Python package can be a bit confusing for beginners. If you have installed a Python package and want to access a static file from that package, this guide will help you with the necessary steps.

## Locate the Package Path

The first thing you need to do is to locate the package path. Python packages are usually installed in the site-packages folder of the Python installation. You can find the site-packages folder by running the following command in your Python terminal:

```
import site; 
print(site.getsitepackages())
```

This command will print a list of directories that includes the site-packages folder.

## Access the File

Once you know the package path, you can access the static file using the following code:

```
import pkg_resources

filename = pkg_resources.resource_filename('packagename', 'filename')
with open(filename) as f:
    data = f.read()
```

In this code, replace `packagename` with the name of the package containing the file, and `filename` with the name of the static file you want to read. The `pkg_resources.resource_filename()` method returns the full path of the static file, which you can then open and read.

## Example

Here's an example of reading a `README.md` file from a package named `mypackage`:

```
import pkg_resources

filename = pkg_resources.resource_filename('mypackage', 'README.md')
with open(filename) as f:
    data = f.read()
    
print(data)
```

This code will print the contents of `README.md` file.

## Conclusion

In this guide, we covered how to read a static file from inside a Python package. By following these steps, you can easily access the static file from any Python package.
