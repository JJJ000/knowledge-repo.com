---
title: What is the most efficient way to convert a string to lowercase in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To lowercase a string in Python, use the lower() method.
---

**Contents**

[TOC]

## Using the Lower() Method
The `lower()` method can be used to convert a string to lowercase.

Example: 

```python
my_string = "HELLO WORLD"

my_string_lower = my_string.lower()

print(my_string_lower)
```

Output: 
`hello world`

## Using the str.translate() Method
The `str.translate()` method can be used to convert a string to lowercase.

Example: 

```python
my_string = "HELLO WORLD"

my_string_lower = my_string.translate(str.maketrans('', '', string.punctuation)).lower()

print(my_string_lower)
```

Output: 
`hello world`

## Using the str.replace() Method
The `str.replace()` method can be used to convert a string to lowercase.

Example: 

```python
my_string = "HELLO WORLD"

my_string_lower = my_string.replace(" ", "").lower()

print(my_string_lower)
```

Output: 
`helloworld`

## Using the str.join() Method
The `str.join()` method can be used to convert a string to lowercase.

Example: 

```python
my_string = "HELLO WORLD"

my_string_lower = ''.join(my_string.lower().split())

print(my_string_lower)
```

Output: 
`helloworld`
