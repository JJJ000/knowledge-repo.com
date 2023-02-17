---
title: The Python JSON encoder changes nans to null instead
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Yes, the Python JSON encoder does convert NaNs to null when encoding to JSON.
---

**Contents**

[TOC]

# Introduction

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to transfer data between two systems. It is an open standard format that is both human-readable and machine-readable. JSON is a text-based format that can be used to represent simple data structures and associative arrays.

# How JSON Encoder Handles NaNs

The JSON encoder is responsible for converting a Python data structure into a JSON string. By default, the JSON encoder will convert any NaN (Not a Number) values to null. This means that any NaN values in the Python data structure will be represented as "null" in the JSON string.

# Advantages of Converting NaNs to Null

One of the advantages of converting NaNs to null is that it helps to maintain the integrity of the data. Without converting NaNs to null, the data could be misinterpreted. For example, if a NaN value is not converted to null, it could be interpreted as a valid number. This could lead to inaccurate results.

Another advantage of converting NaNs to null is that it helps to reduce the size of the JSON string. By converting NaNs to null, the JSON string will be smaller and easier to parse.

# Conclusion

In conclusion, the JSON encoder will convert any NaN (Not a Number) values to null. This helps to maintain the integrity of the data and reduce the size of the JSON string.
