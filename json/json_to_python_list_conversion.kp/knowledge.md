---
title: Transform a JSON array into a Python list
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The json.loads() function can be used to convert a JSON array to a Python list.
---

**Contents**

[TOC]

# Section 1: Overview

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used for data exchange between different applications. It is a text-based, human-readable format that is used to represent simple data structures and associative arrays (also known as objects). JSON is easy to read and write, and is often used to transmit data over a network connection.

# Section 2: JSON Array

A JSON array is a collection of values that are enclosed within square brackets and separated by commas. The values can be strings, numbers, objects, arrays, Boolean values (true or false), or null. Arrays in JSON are almost the same as arrays in JavaScript. In JSON, array values must be of type string, number, object, array, boolean or null.

# Section 3: Python List

In Python, a list is a data structure that holds an ordered collection of items. It is similar to an array in JavaScript, but it can contain mixed types of elements, such as strings, integers, floats, and other objects. Unlike an array, a list can also contain duplicate elements.

# Section 4: Converting JSON Array to Python List

To convert a JSON array to a Python list, you can use the json.loads() method. This method takes a JSON string and returns a Python list. For example, if you have a JSON array such as:

```
[1,2,3,4,5]
```

You can convert it to a Python list like this:

```
import json
my_list = json.loads('[1,2,3,4,5]')
```

The resulting list will be:

```
[1, 2, 3, 4, 5]
```
