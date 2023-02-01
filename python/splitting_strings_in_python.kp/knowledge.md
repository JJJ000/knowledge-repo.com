---
title: In python, divide a string into separate parts based on spaces
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the split() method with the argument ` ` (a single space) to split a string on whitespace in Python.
---

**Contents**

[TOC]

### Using `str.split()`
The `str.split()` method can be used to split a string on whitespace.

### Syntax
```python
str.split(separator, maxsplit)
```

### Parameters
* `separator` - Specifies the separator to use when splitting the string. By default, any whitespace is a separator.
* `maxsplit` - Specifies how many splits to do. The default value of -1 means, no limit.

### Example
```python
# Initializing string 
test_string = "Geeks for Geeks"

# Printing original string 
print("The original string is : " + test_string) 

# Splitting string using split() 
res = test_string.split() 

# Printing result 
print("The split string is : " + str(res)) 
```

Output:
```
The original string is : Geeks for Geeks
The split string is : ['Geeks', 'for', 'Geeks']
```
