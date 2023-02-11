---
title: It is not possible to convert a 'float32' object into a JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The float32 type cannot be serialized into JSON format.
---

**Contents**

[TOC]

## Section 1: What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is used to exchange data between a server and a web application. JSON is based on a subset of the JavaScript programming language and is easy to read and write.

## Section 2: What is a Float32?
A Float32 is a 32-bit floating-point data type. It is used to store decimal values, such as fractions and decimal points. This data type is commonly used in computer programming for numerical calculations.

## Section 3: Why is a Float32 Not JSON Serializable?
A Float32 is not JSON serializable because JSON only supports data types that can be represented as a string. Since a Float32 is a numerical data type, it cannot be converted into a string. Therefore, it cannot be serialized into JSON.

## Section 4: How to Resolve the Issue?
To resolve the issue of a Float32 not being JSON serializable, the data must first be converted into a string. This can be done by using the `str()` function in Python. Once the data has been converted into a string, it can then be serialized into JSON.
