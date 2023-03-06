---
title: In python, what is the method for determining the mime type of a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the Python built-in module mimetypes to find the mime type of a file.
---

**Contents**

[TOC]

## Section 1: Introduction

In this tutorial, we'll learn about finding the MIME type of a file in Python. The MIME type of a file is a string identifier that specifies the type of data stored in a file. This information is important because it tells the computer how to handle the file. For example, the MIME type of a JPEG image file is "image/jpeg", which tells the computer that the file is an image and that it should be treated as such. Python provides several ways to find the MIME type of a file. We'll explore these methods in the sections below.

## Section 2: Using the mimetypes module

The easiest way to find the MIME type of a file in Python is to use the mimetypes module. This module provides a database of known MIME types, and can automatically determine the MIME type of a given file based on its file extension. Here's an example of how to use the mimetypes module:

```python
import mimetypes

filename = "example.pdf"
mime_type, _ = mimetypes.guess_type(filename)
print(mime_type)
```

In this example, we import the mimetypes module and set the filename variable to the name of the file we want to check. We then call the guess_type() function, passing the filename as a parameter. This function returns a tuple containing the MIME type of the file (as a string) and the value None (which we ignore in this case). Finally, we print the MIME type to the console.

## Section 3: Using the magic module

The magic module provides an interface to the Unix file command, which can be used to determine the MIME type of a file. This module requires the installation of the libmagic library, which is not included with Python. Here's an example of how to use the magic module:

```python
import magic

filename = "example.pdf"
mime_type = magic.Magic(mime=True).from_file(filename)
print(mime_type)
```

In this example, we import the magic module and set the filename variable to the name of the file we want to check. We then create a Magic object with the parameter mime=True, which tells the object to return the MIME type of the file. We call the from_file() method of the Magic object, passing the filename as a parameter. This method returns the MIME type of the file as a string. Finally, we print the MIME type to the console.

## Section 4: Using the python-magic-bin library

The python-magic-bin library provides a high-level interface to the libmagic library, which can be used to determine the MIME type of a file. This library can be installed using pip. Here's an example of how to use the python-magic-bin library:

```python
import magic

filename = "example.pdf"
mime_type = magic.from_file(filename, mime=True)
print(mime_type)
```

In this example, we import the magic module (which is now provided by the python-magic-bin library) and set the filename variable to the name of the file we want to check. We then call the from_file() function, passing the filename as a parameter and setting the mime parameter to True. This function returns the MIME type of the file as a string. Finally, we print the MIME type to the console.
