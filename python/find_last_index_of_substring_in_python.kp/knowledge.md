---
title: Locate the final instance of a substring within a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The index of the last occurrence of a substring in a string can be found using the str.rfind() method.
---

**Contents**

[TOC]

### Using str.rfind()
The `str.rfind()` method can be used to find the index of the last occurrence of a substring in a string. 

Syntax:
```
str.rfind(sub[, start[, end]])
```
Parameters:
- `sub` : This is the substring that needs to be searched.
- `start` (Optional) : This is the starting index from where the search begins.
- `end` (Optional) : This is the ending index till which the search continues.

Example:
```
string = "Python is an interpreted, object-oriented, high-level programming language with dynamic semantics"

# find index of last occurrence of 'high-level'
index = string.rfind('high-level')

print("Index of last occurrence of 'high-level' is:", index)

# Output: Index of last occurrence of 'high-level' is: 51
```

### Using rindex()
The `rindex()` method can also be used to find the index of the last occurrence of a substring in a string.

Syntax:
```
str.rindex(sub[, start[, end]])
```
Parameters:
- `sub` : This is the substring that needs to be searched.
- `start` (Optional) : This is the starting index from where the search begins.
- `end` (Optional) : This is the ending index till which the search continues.

Example:
```
string = "Python is an interpreted, object-oriented, high-level programming language with dynamic semantics"

# find index of last occurrence of 'high-level'
index = string.rindex('high-level')

print("Index of last occurrence of 'high-level' is:", index)

# Output: Index of last occurrence of 'high-level' is: 51
```

### Using re.search()
The `re.search()` method can also be used to find the index of the last occurrence of a substring in a string.

Syntax:
```
re.search(pattern, string, flags=0)
```
Parameters:
- `pattern` : This is the substring that needs to be searched.
- `string` : This is the string in which the substring needs to be searched.
- `flags` (Optional) : This is used to modify the matching behavior of the pattern.

Example:
```
import re

string = "Python is an interpreted, object-oriented, high-level programming language with dynamic semantics"

# find index of last occurrence of 'high-level'
match = re.search('high-level', string)

if match:
    index = match.start()
    print("Index of last occurrence of 'high-level' is:", index)

# Output: Index of last occurrence of 'high-level' is: 51
```
