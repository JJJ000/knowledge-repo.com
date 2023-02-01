---
title: Retrieve the final four characters of a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the slicing syntax to get the last 4 characters of a string string[-4].
---

**Contents**

[TOC]

### Using Slicing

We can use slicing to get the last 4 characters of a string in Python. The syntax for this is `string[start:end:step]`, where `start` is the starting index of the substring, `end` is the ending index of the substring, and `step` is the number of characters to move forward after each iteration. In this case, we can set `start` to `-4` to start 4 characters from the end of the string, and `end` to `None` to indicate the end of the string. The `step` can be left out since we want to take every character.

```python
string = "This is a string"
last_four = string[-4:]

print(last_four) # Output: "ring"
```

### Using Negative Indexing

We can also use negative indexing to get the last 4 characters of a string in Python. Negative indexing starts from the end of the string, so `-1` will refer to the last character, `-2` to the second-last character, and so on. This allows us to access the last 4 characters of the string by specifying the indices `-4`, `-3`, `-2`, and `-1`.

```python
string = "This is a string"
last_four = string[-4:-1]

print(last_four) # Output: "rin"
```

### Using `len()`

We can also use the `len()` function to get the last 4 characters of a string in Python. The `len()` function returns the length of a string, so we can subtract 4 from it to get the index of the fourth-last character. We can then use this index to access the last 4 characters of the string.

```python
string = "This is a string"
last_four = string[len(string)-4:]

print(last_four) # Output: "ring"
```

### Using `str.slice()`

Finally, we can use the `str.slice()` method to get the last 4 characters of a string in Python. The `str.slice()` method takes two arguments, `start` and `stop`, which indicate the starting and ending indices of the substring, respectively. We can set `start` to `-4` to start 4 characters from the end of the string, and `stop` to `None` to indicate the end of the string.

```python
string = "This is a string"
last_four = string.slice(-4, None)

print(last_four) # Output: "ring"
```
