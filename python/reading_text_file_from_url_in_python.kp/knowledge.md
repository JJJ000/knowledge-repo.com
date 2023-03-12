---
title: What is the easiest method to access the contents of a text file using a url?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The simplest way to read the contents of a text file from a URL in Python is to use the urllib.request library to open and read the file.
---

**Contents**

[TOC]

## Importing the urllib library

The urllib library provides a set of functions to interact with URLs. We will be using it to read the contents of a text file from a URL.

```python
import urllib.request
```


## Reading text from URL

First, we will define the URL of the text file that we want to read.

```python
url = 'http://example.com/file.txt'
```

Next, we will use the `urlopen()` function to open the URL and read its contents.

```python
with urllib.request.urlopen(url) as response:
   contents = response.read().decode('utf-8')  
```

The `with` statement is used to automatically close the response object when we are done reading its contents. The `decode()` function is used to convert the bytes read from the URL into a string using the UTF-8 encoding.

The variable `contents` now contains the contents of the text file.


## Full code

```python
import urllib.request

url = 'http://example.com/file.txt'

with urllib.request.urlopen(url) as response:
   contents = response.read().decode('utf-8')  

print(contents)
```
