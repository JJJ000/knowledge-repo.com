---
title: How can I access the data on my google drive through google colab?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the following code snippet to read data from Google Drive in Python using Google Colab 

```
from google.colab import drive 
drive.mount(`/content/drive`)
```
---

**Contents**

[TOC]

### Mounting Google Drive to Colab

The first step to accessing data from your Google Drive in Python via Google Colab is to mount your drive. To do this, you have to execute the following code:

```
from google.colab import drive
drive.mount('/content/drive')
```

When you run this code snippet, Colab will prompt you to authenticate yourself with your Google account, and allow Colab to access your Google Drive.

Once you have successfully authenticated and given permission to Colab, your Google Drive directory will be mounted at the path `/content/drive/`.

### Accessing files

After mounting the Google Drive, you can access the files on it by specifying the path to the file. For instance, if you have a file called `example.txt` in your Google Drive's root directory, you can access it using the following code:


```
with open('/content/drive/My Drive/example.txt', 'r') as f:
    print(f.read())
```

In this example, we are using the `open()` function to open the file `example.txt` and reading its contents with the `read()` function.

However, it is worth noting you need to specify the path with your entire Google Drive directory, beginning with `/content/drive/My Drive/`. 


### Copying files

In certain cases, you might need to copy one or more files from your Google Drive to Colab's virtual machine file system. You can do this using the `shutil` standard library module in Python. 

This module provides easy-to-use functions to perform high-level file operations such as copying, moving, and deleting files.

To copy a file from your Google drive to Colab, you can execute the following code:

```
import shutil

# source path in Google Drive
src_path = '/content/drive/My Drive/example.txt'

# destination path in Colab's virtual machine file system
dst_path = '/content/example.txt'

# copy source file to destination file
shutil.copyfile(src_path, dst_path)
```

Here, we are using `shutil.copyfile()` function to copy the file `example.txt` from our Google Drive to Colab's virtual machine file system.

After copying the file, you can access it in the same way as we did earlier - by using the `open()` and `read()` functions: 

```
with open('/content/example.txt', 'r') as f:
    print(f.read())
```

This code will read the contents of the file `example.txt` from Colab's virtual machine file system.
