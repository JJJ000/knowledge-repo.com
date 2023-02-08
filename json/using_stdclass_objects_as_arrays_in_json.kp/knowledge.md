---
title: It is not possible to treat an object of type stdclass as an array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: No, you cannot use an object of type stdClass as an array in JSON.
---

**Contents**

[TOC]

# Section 1: What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format used for exchanging data between a server and a web application. It is a text-based, human-readable format for representing simple data structures and associative arrays.

# Section 2: What is an Object of Type stdClass?
An object of type stdClass is a special type of object that is created by PHP when it encounters an undefined class. It is used to store data in an object-oriented manner and can be accessed using object notation.

# Section 3: What is the Error?
The error occurs when trying to access an element of an object of type stdClass as an array. This is because stdClass objects are not arrays and do not have array-like properties.

# Section 4: How to Fix the Error?
The error can be fixed by converting the stdClass object to an array before attempting to access its elements. This can be done using the `(array)` casting operator or the `json_decode()` function.
