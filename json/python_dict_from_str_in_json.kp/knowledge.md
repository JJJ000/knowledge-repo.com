---
title: Convert a string to a dictionary in python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Convert a JSON string to a dictionary in Python by using the json.loads() method.
---

**Contents**

[TOC]

## Section 1: Overview

A JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to store and exchange data. It is based on a subset of the JavaScript programming language and is easy to read and write. JSON objects are composed of key-value pairs, with the key being a string and the value being either a string, number, boolean, array, or object.

## Section 2: Converting a String to a Dictionary

The most common way to convert a string to a dictionary in Python is to use the json.loads() method. This method takes a string as an argument and returns a dictionary object. For example, the following string:

```
"{'name': 'Bob', 'age': 25}"
```

can be converted to a dictionary with the following code:

```
import json

person = json.loads("{'name': 'Bob', 'age': 25}")

print(person)
```

The output will be:

```
{'name': 'Bob', 'age': 25}
```

## Section 3: Other Ways to Convert a String to a Dictionary

There are other ways to convert a string to a dictionary in Python. For example, the ast.literal_eval() method can be used to evaluate a string and return a dictionary. This method takes a string as an argument and returns the result of evaluating the string as a Python expression. For example, the following string:

```
"{'name': 'Bob', 'age': 25}"
```

can be converted to a dictionary with the following code:

```
import ast

person = ast.literal_eval("{'name': 'Bob', 'age': 25}")

print(person)
```

The output will be:

```
{'name': 'Bob', 'age': 25}
```

## Section 4: Conclusion

In conclusion, there are several ways to convert a string to a dictionary in Python. The json.loads() method is the most common way, but the ast.literal_eval() method can also be used. Both of these methods take a string as an argument and return a dictionary object.
