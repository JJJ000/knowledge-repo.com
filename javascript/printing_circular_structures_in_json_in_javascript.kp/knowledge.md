---
title: What is the best way to print a circular structure in a json-like format?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use a recursive function to traverse the circular structure and print each node in a JSON-like format.
---

**Contents**

[TOC]

**Option 1: Using Recursion**

1. Create a function that takes in the circular structure as an argument.
2. Create an empty object to store the JSON-like structure.
3. Iterate through the circular structure and add the key-value pairs to the empty object.
4. If the value of a key is an object, call the function again with the value as an argument.
5. Return the object.

**Option 2: Using a Library**

1. Install a library that can serialize circular structures, such as CircularJSON.
2. Import the library into your project.
3. Use the library's serialize method to serialize the circular structure.
4. Return the serialized structure.
