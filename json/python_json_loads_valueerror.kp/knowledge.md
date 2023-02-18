---
title: The Python json.loads function is giving an error of 'valueerror invalid control character at line 1 column 33 (char 33)'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: The JSON string contains an invalid control character which needs to be removed before being parsed.
---

**Contents**

[TOC]

1. Overview
2. Causes
3. Solutions
4. Resources

## Overview
When using the `json.loads()` function in Python, a `ValueError: Invalid control character at: line 1 column 33 (char 33)` can occur. This error is caused by an invalid character in the JSON string being processed.

## Causes
The `ValueError: Invalid control character at: line 1 column 33 (char 33)` error is caused by an invalid character in the JSON string being processed. This can be caused by a non-printable character in the string, such as a tab or carriage return. It can also be caused by an invalid escape sequence, such as "\x".

## Solutions
The solution to this error is to make sure that the JSON string being processed does not contain any invalid characters. This can be done by using a JSON validator to check the string for any invalid characters.

## Resources
- [JSON Validator](https://jsonlint.com/)
- [Python Documentation: json.loads()](https://docs.python.org/3/library/json.html#json.loads)
