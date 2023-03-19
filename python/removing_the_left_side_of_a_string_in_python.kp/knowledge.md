---
title: What is the procedure for eliminating the left section of a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use string slicing with the starting index to remove the left part of a string in Python.
---

**Contents**

[TOC]

# Introduction

In Python, we can remove the left part of a string by using various built-in string methods. In this guide, we will go through some of the methods that can be used to accomplish this task.

# Using String Slicing

One of the simplest and most straightforward ways to remove the left part of a string is to use string slicing. We can use the slice notation to remove a portion of the string from the left. Here is an example:

```
string = "Hello, World!"
new_string = string[7:]
print(new_string) # OUTPUT: "World!"
```

In this example, we created a string variable called `string` that contains the text "Hello, World!". We then used string slicing to remove the first seven characters of the string, leaving only the right part of the string. The resulting string is then stored in a new variable called `new_string`.

# Using String Methods

Python provides various string methods that can be used to remove the left part of a string. Here are some of the most commonly used methods:

## Using the `split()` Method

We can use the `split()` method to split a string into a list of substrings based on a specified separator. By specifying a separator that occurs at the point where we want to remove the left part of the string, we can create a new string that contains only the right part of the original string. Here is an example:

```
string = "Hello, World!"
new_string = string.split(", ")[1]
print(new_string) # OUTPUT: "World!"
```

In this example, we used the `split()` method with a comma and a space as the separator. This splits the original string into two substrings: "Hello" and "World!". We then accessed the second substring using the index `[1]`, which contains only the right part of the original string.

## Using the `partition()` Method

Another string method that can be used to remove the left part of a string is the `partition()` method. This method splits a string into three parts based on a specified separator and returns a tuple containing the three parts. The first part of the tuple contains the left part of the string before the separator, the second part contains the separator itself, and the third part contains the right part of the string after the separator. Here is an example:

```
string = "Hello, World!"
new_string = string.partition(", ")[2]
print(new_string) # OUTPUT: "World!"
```

In this example, we used the `partition()` method with a comma and a space as the separator. This splits the original string into three parts: "Hello", ", ", and "World!". We then accessed the third part of the tuple using the index `[2]`, which contains only the right part of the original string.

# Conclusion

In this guide, we have gone through some of the methods that can be used to remove the left part of a string in Python. By using string slicing or various string methods like `split()` and `partition()`, we can easily create new strings that contain only the right part of the original string.
