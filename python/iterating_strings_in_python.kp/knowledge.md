---
title: Looping through each character in a string using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can iterate each character in a string using a for loop, such as `for char in string`.
---

**Contents**

[TOC]

## Using a For Loop

Using a for loop is a simple way to iterate through each character in a string.

```python
# Define the string 
string = "Hello World!"

# Iterate through each character in the string
for char in string:
    print(char)

# Output
H
e
l
l
o
 
W
o
r
l
d
!
```

## Using a While Loop

Using a while loop is another way to iterate through each character in a string.

```python
# Define the string 
string = "Hello World!"

# Set the index to 0
i = 0

# Iterate through each character in the string
while i < len(string):
    print(string[i])
    i += 1

# Output
H
e
l
l
o
 
W
o
r
l
d
!
```

## Using a List Comprehension

Using a list comprehension is a more concise way to iterate through each character in a string.

```python
# Define the string 
string = "Hello World!"

# Iterate through each character in the string
[print(char) for char in string]

# Output
H
e
l
l
o
 
W
o
r
l
d
!
```

## Using the map() Function

Using the map() function is another concise way to iterate through each character in a string.

```python
# Define the string 
string = "Hello World!"

# Iterate through each character in the string
list(map(print, string))

# Output
H
e
l
l
o
 
W
o
r
l
d
!
```
