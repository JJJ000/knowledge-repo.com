---
title: Change a string key to an integer in a dictionary
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Use the built-in JSON.parse() method and pass a reviver function to convert the string key to an int.
---

**Contents**

[TOC]

## Section 1: Understanding the Problem

The problem is to convert a string key to an integer in a Dictionary in JSON. JSON is a data interchange format that stores data in a hierarchical structure, and dictionaries are a type of data structure that stores data as key-value pairs. A string key is a key that is stored as a string (i.e. a sequence of characters) and an integer is a whole number that can be positive, negative, or zero.

## Section 2: Converting the String Key to Integer

The process of converting a string key to an integer in a Dictionary in JSON involves two steps: first, the string key must be converted to an integer; then, the integer must be used as the new key in the Dictionary. To convert a string key to an integer, the `parseInt()` function can be used. This function takes a string as its argument and returns an integer.

## Section 3: Updating the Dictionary

Once the string key has been converted to an integer, the next step is to update the Dictionary with the new key. The `set()` method can be used to add a new key-value pair to the Dictionary. This method takes two arguments: the key and the value. In this case, the key should be the integer that was just created and the value should be the value associated with the original string key.

## Section 4: Example

Here is an example of how to convert a string key to an integer in a Dictionary in JSON:

```json
let dict = {
  "foo": "bar"
};

let intKey = parseInt("foo");
dict.set(intKey, dict.get("foo"));

// dict is now {1: "bar"}
```

In this example, the string key `"foo"` is converted to an integer using the `parseInt()` function. Then, the `set()` method is used to add a new key-value pair to the Dictionary, with the integer as the key and the value associated with the original string key as the value.
