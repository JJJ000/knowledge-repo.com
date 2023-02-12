---
title: What is the result of parsing the string '1234' using json.parse?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: JSON.parse([`1234`]) returns 1234 because it is parsing a string of the number 1234 into a number data type.
---

**Contents**

[TOC]

# Overview
JSON.parse() is a method used to convert a JSON string into a JavaScript object. In this case, the input is an array with a single element, '1234'. When JSON.parse() is applied to this array, it returns the single element of the array, which is '1234'.

# How JSON.parse() Works
JSON.parse() is a method that takes a JSON string as an argument and returns a JavaScript object. The JSON string is parsed and the data is converted into a JavaScript object. This object can then be used to access the data contained in the JSON string.

# What Happens When JSON.parse() is Applied to an Array
When JSON.parse() is applied to an array, it returns the first element of the array. This is because the array is treated as a single element, and the first element is returned. In this case, the array contains a single element, '1234', so JSON.parse() returns '1234'.

# Conclusion
JSON.parse() is used to convert a JSON string into a JavaScript object. When applied to an array, it returns the first element of the array. In this case, the array contains a single element, '1234', so JSON.parse() returns '1234'.
