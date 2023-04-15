---
title: What is the best way to add more content to a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To append to a file in Python, use the `append` mode when opening the file with the open() function.
---

**Contents**

[TOC]

### Using the Open Function

The `open()` function is used to open a file and then use the `.write()` function to append data to the file.

```python
# open the file in append mode 
f = open("sample.txt", "a") 
  
# append additional data to the file 
f.write("This is an additional line of text.") 
  
# close the file 
f.close() 
```

### Using the Append Mode

The `open()` function can also be used in append mode to directly append data to the file.

```python
# open the file in append mode 
f = open("sample.txt", "a") 
  
# append additional data to the file 
f.write("This is an additional line of text.") 
  
# close the file 
f.close() 
```

### Using the With Statement

The `with` statement can be used to open a file and then use the `.write()` function to append data to the file.

```python
# open the file in append mode 
with open("sample.txt", "a") as f: 
  
    # append additional data to the file 
    f.write("This is an additional line of text.") 
```

### Using the Print Function

The `print()` function can be used to append data to a file.

```python
# open the file in append mode 
with open("sample.txt", "a") as f: 
  
    # append additional data to the file 
    print("This is an additional line of text.", file = f) 
```
