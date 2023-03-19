---
title: What is the method to obtain all the text following the final forward slash in a url?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can use the split() method to split the URL by the slash, and then access the last element using negative indexing.
---

**Contents**

[TOC]

## 1. Split the URL by slashes

To get everything after the last slash in a URL, we need to first split the URL into individual components separated by slashes. The `split()` method can be used to do this, which takes a separator as an argument and returns a list of components.

```python
url = "https://www.example.com/path/to/file.html"

components = url.split("/")
print(components)
```
This will output:
```
['https:', '', 'www.example.com', 'path', 'to', 'file.html']
```

## 2. Get the last component

In the above list of components, the last one will be the one we're interested in. We can access it using negative indexing, where `-1` refers to the last item.

```python
last_component = components[-1]
print(last_component)
```
This will output:
```
file.html
```

## 3. Extract the file extension (optional)

If we only want to get the file name and not the extension, we can split the last component by the dot separator and take the first part.

```python
file_name = last_component.split(".")[0]
print(file_name)
```
This will output:
```
file
```

## 4. Full code

Putting it all together, the code to get everything after the last slash in a URL can be written as:

```python
url = "https://www.example.com/path/to/file.html"
components = url.split("/")
last_component = components[-1]
file_name = last_component.split(".")[0]
print(file_name)
```
This will output:
```
file
```
