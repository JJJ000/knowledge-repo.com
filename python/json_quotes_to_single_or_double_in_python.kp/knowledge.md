---
title: Comparison of using single and double quotes in json
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In JSON, double quotes are used for representing strings and single quotes are not valid.
---

**Contents**

[TOC]

Single versus Double Quotes in JSON in Python

Introduction

JSON stands for JavaScript Object Notation, and it's the most widely used data format for sending and receiving information. JSON uses a key-value pair format, where the keys are in the form of strings enclosed in single or double quotes. In Python, single and double quotes are used interchangeably to represent strings, but when writing JSON, which one should be used? In this article, we'll explore the difference between single and double quotes and their usage in JSON in Python.

Single Quotes

In Python, single quotes are used to represent strings, but they can also be used in JSON. When using single quotes in JSON, it is important to ensure that any internal strings, such as those within the value of a key-value pair, are properly enclosed in double quotes. Failure to do so can result in an error when parsing the JSON data. For instance, the following JSON snippet uses single quotes for both the key and the value:

`{'name': 'John', 'age': 30}`

In this case, it is perfectly valid JSON. However, if the value were to contain a string itself, it must be properly enclosed in double quotes. For example:

`{'name': 'John', 'address': '{"street": "123 Main St", "city": "Anytown"}`

In this example, a single quote is used for the `name` key and its value, and a double quote is used for the `address` key and its value. The value of the `address` key is a string, and it contains double quotes around the street and city, in order to properly represent the JSON data.

Double Quotes

Double quotes are the more widely used quotes when writing JSON as they present less ambiguity and are easier to work with. They are also the de facto standard for JSON representation. When using double quotes in JSON, it is essential that all strings are properly enclosed in double quotes, which is generally easy to do in most cases, for instance:

`{"name": "John", "age": 30}`

In this example, double quotes are used for both the key and the value of each key-value pair, making it a valid and properly formatted JSON string.

Conclusion

In Python, both single and double quotes can be used to represent strings. However, when it comes to JSON, the de facto standard is to use double quotes, and single quotes should only be used when necessary, such as in cases where the JSON data contains internal strings that need to be enclosed in double quotes. Regardless of the quotes used in JSON, it is important to ensure that all strings are properly enclosed to avoid any parsing errors.
