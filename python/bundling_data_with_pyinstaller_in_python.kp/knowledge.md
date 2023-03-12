---
title: The process of incorporating data files into pyinstaller through the use of "--onefile" option
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `--add-data` option followed by the path to the data file and the directory or path where you want it to be located in the bundled executable.
---

**Contents**

[TOC]

## Section 1: Introduction

When creating a standalone executable file of a Python application using PyInstaller, it is often necessary to include additional data files such as images, config files or other resources. This can be done using the `--add-data` option in PyInstaller. However, if you want to create a single executable file, the `--onefile` option needs to be used. In this scenario, it may not be clear how to include the required data files. In this tutorial, we will explore how to bundle data files with PyInstaller `--onefile` option.

## Section 2: Using the --add-data option

The `--add-data` command-line option is used to indicate any data files to be included in the bundle. The general syntax for using this option is as follows:

```python
pyinstaller --add-data "path/to/data_files;path/in/bundle" scriptname.py
```

The first part of the string `path/to/data_files` represents the path to the data file(s) to be included in the bundle. The second part `path/in/bundle` represents the path at which to place the data file(s) in the bundle. In other words, when the executable is created, the data files will be located at this path relative to the executable.

For example, let's say you have an image file called `logo.png` located in the `images` directory, and you want to include this file in the bundle. The command to achieve this will be as follows:

```python
pyinstaller --add-data "images/logo.png;images/" scriptname.py
```

This will include the `logo.png` image in the `images` directory within the executable bundle.

## Section 3: Using the resource_path function

The `resource_path` function can be used to determine the path to the data files at runtime. This function takes the filename of the resource and returns the full path to the resource in the application's data directory. This is particularly useful when the application is run from a different directory or on another machine where the paths to the resources may not be the same as during development.

Here is an example implementation of the `resource_path` function:

```python
import sys
import os

def resource_path(relative_path):
    """ Get absolute path to resource, works for dev and for PyInstaller """
    try:
        # PyInstaller creates a temp folder and unpacks the executable in it, 
        # so we need to detect if we are in a bundle or not, depending on
        # how the application is run, to get the correct path to the resource
        base_path = sys._MEIPASS
    except Exception:
        base_path = os.path.abspath(".")
    
    return os.path.join(base_path, relative_path)
```

You can then use this function in your code to load the data files, for example:

```python
import pygame   # import library to display images

# assuming we have an image called logo.png in the images directory

# use the resource_path function to get the full path to the image
image_path = resource_path("images/logo.png")

# load the image using pygame
image = pygame.image.load(image_path)

# display the image
pygame.display.set_mode((image.get_width(), image.get_height()))
pygame.display.set_caption("My Image")
pygame.display.flip()
pygame.time.delay(5000)
```

## Section 4: Conclusion

In conclusion, we have seen how to include data files in a PyInstaller bundle using the `--add-data` option, and how to use the `resource_path` function to access the data files at runtime. This will enable you to create standalone executable files of your Python applications with all the required data included, and ensure that the application runs as expected regardless of the environment.
