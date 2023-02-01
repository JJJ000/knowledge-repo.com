---
title: What is the syntax for finding the index of a character in a Python string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the index() method to get the position of a character in Python.
---

**Contents**

[TOC]

#1 Using the index() Method

The index() method is used to find the index of a character in a string. This method takes a single argument and returns the index of the first occurrence of the character in the string.

Syntax:

string.index(character)

Example:

string = "Hello World!"

print(string.index("W"))

# Output
6

#2 Using the find() Method

The find() method is similar to the index() method, but instead of returning the index of the first occurrence of the character, it returns -1 if the character is not found in the string.

Syntax:

string.find(character)

Example:

string = "Hello World!"

print(string.find("W"))

# Output
6
