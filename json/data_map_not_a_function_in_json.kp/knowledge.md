---
title: 'data.map' is not a recognized function
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: The map() method is not available for JSON objects.
---

**Contents**

[TOC]

**Section 1: What is JSON?**

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and associative arrays (called objects).

**Section 2: What is the .map Function?**

The .map() function is a built-in JavaScript function that can be used to iterate over an array and apply a function to each element. It is commonly used for transforming data from one format to another.

**Section 3: Why Can't .map be Used on JSON?**

JSON is not an array, so it cannot be iterated over using the .map() function. JSON is a data-interchange format, and it does not contain any built-in functions for manipulating data.

**Section 4: How Can Data from JSON be Manipulated?**

Data from JSON can be manipulated using JavaScript functions such as .forEach(), .filter(), and .reduce(). These functions can be used to iterate over the data and apply a function to each element.
