---
title: The bytes object cannot be converted into a JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The bytes object must be decoded into a string before it can be serialized into JSON.
---

**Contents**

[TOC]

## Section 1: What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to store and exchange data. It is based on a subset of the JavaScript programming language and is a text-based, human-readable format. It is used to represent data structures and objects, and is commonly used in web applications to send and receive data.

## Section 2: What is a TypeError?
A TypeError is an error that occurs when a value is not of the expected type. For example, if a function is expecting a string but is given a number, it will throw a TypeError.

## Section 3: What is the 'Object of type 'bytes' is not JSON serializable' Error?
The 'Object of type 'bytes' is not JSON serializable' error occurs when a value of type 'bytes' is passed to the json.dumps() function. This function expects a value that can be serialized as a JSON object, but the 'bytes' type cannot be serialized.

## Section 4: How to Solve the Error
The error can be solved by converting the 'bytes' value to a string before passing it to the json.dumps() function. This can be done using the str() function, which will convert the 'bytes' value to a string.
