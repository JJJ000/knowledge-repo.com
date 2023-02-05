---
title: What is the process for obtaining a string that follows a particular substring?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the str.split() method to split the string at the specific substring, then use the resulting list to access the string after the substring.
---

**Contents**

[TOC]

#1 Using String Slicing

String slicing is a powerful tool to access and manipulate substrings in Python. It allows us to extract a string after a specific substring by specifying the starting and ending index of the desired substring.

To get a string after a specific substring, we need to first find the index of the substring in the original string. We can use the `find()` or `index()` method to find the index of the substring.

Once the index of the substring is found, we can use the `[start:end]` slicing notation to extract the required substring from the original string. The `start` index should be the index of the substring plus one, and the `end` index should be the length of the original string.

#2 Using the `split()` Method

The `split()` method is another useful tool to get a string after a specific substring in Python. This method splits a string into substrings based on a specified separator, and returns a list of the substrings.

To get a string after a specific substring, we need to specify the substring as the separator in the `split()` method. This will return a list of substrings, with the desired substring at the beginning of the list. We can then access the required substring by indexing the list.

#3 Using Regular Expressions

Regular expressions are a powerful tool for pattern matching and string manipulation in Python. They allow us to search for patterns in strings and extract the desired substrings.

To get a string after a specific substring, we need to use the `re.search()` method to search for the substring in the original string. This method will return a `Match` object if the substring is found. We can then use the `.group()` method to extract the string after the substring.

#4 Using the `split()` Method with Regular Expressions

The `split()` method can also be used with regular expressions to get a string after a specific substring. To do this, we need to specify the regular expression pattern of the substring as the separator in the `split()` method. This will return a list of substrings, with the desired substring at the beginning of the list. We can then access the required substring by indexing the list.
